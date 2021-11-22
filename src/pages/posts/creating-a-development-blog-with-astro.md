---
date: 2021-11-22T15:27:43+01:00
tags:
- astro
- frontend
- ssg
- typescript
layout: "../../layouts/post.astro"
title: "Creating a development blog with Astro \U0001F680"
description: What better way to explore a new architecture than a personal playground.
  Progressive enchacement with the islands architecture.
cover: "/assets/img/astro.webp"
setup: ''

---
### Another framework? 🙄

Not exactly, [astro.build](https://astro.build/) works like static site generators ([11ty](https://www.11ty.dev/), [HUGO](https://gohugo.io/)). The build produces no javascript by default, rendering is done at build time, the idea being to make it more difficult for developers to create sites with unnecessarily large bundles and jank user experience. 