---
layout: post
title: "Running Jekyll in Docker (Podman)"
date: 2024-04-07 22:17:00+02:00
categories: jekyll
tags: jekyll docker podman github-pages
---

{% include figure.html url="https://imgs.xkcd.com/comics/containers.png" alt="A comic slightly related to this post is XKCD 1988: Containers" %}

---

Inspired by a [repository](https://github.com/peteretelej/jekyll-container) from Peter Etelej. Adjusted to work with Podman which is what I use on Fedora Workstation as an alternative for Docker.

The version of Ruby and Bundler is important so that it works together with Github Pages and its [dependencies](https://pages.github.com/versions/).

Draft posts are enabled.  
Create a Dockerfile with the following content:

~~~dockerfile
FROM ruby:2.7.4

LABEL maintainer="Tjeu"
LABEL version="1.0"

RUN apt-get -qq update && \
    apt-get -qq install nodejs -y && \
    gem install -q bundler -v 2.4.22

RUN mkdir -p /etc/jekyll && \
    printf 'source "https://rubygems.org"\ngem "github-pages", group: :jekyll_plugins' > /etc/jekyll/Gemfile && \
    printf "\nBuilding requires Ruby gems. Please wait..." && \
    bundle install --gemfile /etc/jekyll/Gemfile --quiet

RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENV BUNDLE_GEMFILE /etc/jekyll/Gemfile

EXPOSE 4000

ENTRYPOINT ["bundle", "exec"]

CMD ["jekyll", "serve","--host=0.0.0.0", "--drafts"]
~~~

Build the container and give it a name.

~~~bash
podman build -f Dockerfile -t tjeu/jekyll .
~~~

Run it!

~~~bash
podman run --rm -it -p 4000:4000 -v "$PWD":/app:z -w /app localhost/tjeu/jekyll:latest
~~~

:z handles SELinux labels when using Podman. This solved for me an error related to permissions. When you accidentally run it without that suffix, the labels will be wrong. I had trouble getting it to work after that and had to delete the folder and run it again to finally get it to work.
