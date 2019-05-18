---
title: "Hugo 0.55.6: One Bug Fix!"
subtitle: Fixes some reported paginator crashes in server mode
date: 2019-05-18T14:23:52+02:00
draft: false
slug: hugo-055-6
author: tomaja
---

This is a bug-fix release with one important fix. There have been reports about infrequent paginator crashes when running the Hugo server since 0.55.0. The reason have been narrowed down to that of parallel rebuilds. This isn’t a new thing, but the changes in 0.55.0 made it extra important to serialize the page initialization. This release fixes that by protecting the Build method with a lock when running in server mode.

#### You can fetch new Hugo version as usuall or go to 
[https://github.com/gohugoio/hugo/releases](https://github.com/gohugoio/hugo/releases)


*Source:* [gohugo.io](https://gohugo.io)



