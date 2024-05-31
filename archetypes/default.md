---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
date: {{ .Date }}
draft: true
image: "https://picsum.photos/800/600" ## replace this with an image in static/images/posts/ (/images/posts/)
description: "" ## description for meta tag
summary: "" ## summary for posts page and recent posts
author:
  name: "" ## name of author
  image: "" ## image of author, located in static/images/author/ (/images/author/)
tags:
  - example
  - another
toc: true ## if you want a table of contents on the side
canonicalUrl: "" ## where post was first published, if applicable
---
