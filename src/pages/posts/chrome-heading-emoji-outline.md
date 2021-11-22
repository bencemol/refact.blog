---
date: 2021-11-22T19:15:43.000+01:00
tags:
- workaround
- chrome
- frontend
layout: "../../layouts/post.astro"
title: "Fix chrome outline emoji style in html headings <em>\U0001F648</em>"
description: Chrome decided to switch to outline styles in heading tags, let's fix
  it!
cover: "/assets/img/chrome-emoji-heading.webp"
setup: ''

---
### Font-weight: initial

Wrapping our emojis in `<em>` tags allows for seperate styling.
A simple `<span>` would be the best semantically, but since I'm generating my content from markdown files with [Astro](https://astro.build/), this was the easiest solution.
`*🙃*` or `_🙃_` in markdown outputs `<em>🙃</em>` in html.

```html
<style>
  em {
    font-weight: initial;
    text-decoration: none;
  }
</style>
<h1>
    Fix chrome outline emoji style in html headings <em>🙈</em>
</h1>
```

Applying `font-weight: initial` resets the style from outline to normal.