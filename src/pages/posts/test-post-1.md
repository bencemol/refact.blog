---
date: 2021-11-05T14:56:03.000+01:00
tags:
- test
- frontend
- ipsum
title: Veritatis pariatur delectus
description: molestiae ipsa aut voluptatibus pariatur dolor nihil ullam nobis libero sapiente ad optio sint suscipit repellat esse quibusdam voluptatem incidunt distinctio vitae autem nihil ut molestias quo
cover: /assets/img/azva3uz.webp
layout: "../../layouts/post.astro"
setup: |
  import Tooltip from "../../components/Tooltip.astro";
  import { Markdown } from 'astro/components';
---
## This will be a bit smaller

### Even smaller than that

#### We're getting there

##### Oh boi

```typescript
const world = 'World';
console.log(`Hello ${world}!`);
```

nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
repudiandae totam in est sint `facere` fuga
earum doloribus ea doloremque quis

<Tooltip text="tooltip text" class="bottom">
  <Markdown> 
  nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
  repudiandae totam in est sint `facere` fuga
  earum doloribus ea doloremque quis
  </Markdown>
</Tooltip>

> nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
repudiandae totam in est sint `facere` fuga
earum doloribus ea doloremque quis
nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
repudiandae totam in est sint `facere` fuga
earum doloribus ea doloremque quis
nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
repudiandae totam in est sint `facere` fuga
earum doloribus ea doloremque quis
nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
repudiandae totam in est sint `facere` fuga
earum doloribus ea doloremque quis
nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
repudiandae totam in est sint `facere` fuga
earum doloribus ea doloremque quis

| Feature                      | Astro                                      | JSX                                                |
| ---------------------------- | ------------------------------------------ | -------------------------------------------------- |
| File extension               | `.astro`                                   | `.jsx` or `.tsx`                                   |
| User-Defined Components      | `<Capitalized>`                            | `<Capitalized>`                                    |
| Expression Syntax            | `{}`                                       | `{}`                                               |
| Spread Attributes            | `{...props}`                               | `{...props}`                                       |
| Boolean Attributes           | `autocomplete` === `autocomplete={true}`   | `autocomplete` === `autocomplete={true}`           |
| Inline Functions             | `{items.map(item => <li>{item}</li>)}`     | `{items.map(item => <li>{item}</li>)}`             |
| IDE Support                  | WIP - [VS Code][code-ext]                  | Phenomenal                                         |
| Requires JS import           | No                                         | Yes, `jsxPragma` (`React` or `h`) must be in scope |
| Fragments                    | Automatic top-level, `<>` inside functions | Wrap with `<Fragment>` or `<>`                     |
| Multiple frameworks per-file | Yes                                        | No                                                 |
| Modifying `<head>`           | Just use `<head>`                          | Per-framework (`<Head>`, `<svelte:head>`, etc)     |
| Comment Style                | `<!-- HTML -->`                            | `{/* JavaScript */}`                               |
| Special Characters           | `&nbsp;`                                   | `{'\xa0'}` or `{String.fromCharCode(160)}`         |
| Attributes                   | `dash-case`                                | `camelCase`                                        |
