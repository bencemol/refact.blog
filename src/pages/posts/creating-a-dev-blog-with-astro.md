---
date: 2021-11-22T15:27:43.000+01:00
tags:
  - astro
  - frontend
  - ssg
  - typescript
layout: '../../layouts/post.astro'
title: "Creating a developer blog with Astro <em>\U0001F680</em>"
description:
  What better way to explore a new architecture than a personal playground?
  Progressive enchacement with the islands architecture.
cover: '/assets/img/astro.webp'
---

### Another framework? _🙄_

Not exactly, [Astro](https://astro.build/) works more like static site generators ([11ty](https://www.11ty.dev/), [HUGO](https://gohugo.io/)).
The build produces no javascript by default, rendering is done at build time, the idea being to make it more difficult for developers to create sites with unnecessarily large bundles and jank user experience.

### What about interactivity?

Sure, most content on the web could be rendered statically, but the web would be a pretty boring place without _some_ javascript. Astro solves [progressive enchacement](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement) through the [islands architecture](https://jasonformat.com/islands-architecture/). You can choose to hydrate specific components with javascript in the browser, just mark the component with the `client:` directive and select a hydration strategy.

| Strategy               | Hydration                                                                                                                            | Prerendered |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ----------- |
| `client:load`          | on page load                                                                                                                         | ✔️          |
| `client:idle`          | when main thread is free <br> [requestIdleCallback](https://developer.mozilla.org/en-US/docs/Web/API/Window/requestIdleCallback)     | ✔️          |
| `client:visible`       | when element enters viewport <br> [IntersectionObserver](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API) | ✔️          |
| `client:media={QUERY}` | when browser matches media query                                                                                                     | ✔️          |
| `client:only`          | on page load                                                                                                                         | ❌          |

```astro
---
// Example: hydrating a Svelte component in the browser.
import SvelteComponent from '../components/SvelteComponent.svelte';
---
<!-- "client:visible" means the component won't load any client-side
     JavaScript until it becomes visible in the user's browser. -->
<SvelteComponent client:visible />
```

But how does [Svelte](https://svelte.dev/) come into the picture?

### Framework agnostic

To build your components, Astro gives you the option to use any of:

- React
- Svelte
- Vue
- Preact
- Web Components
- Plain old HTML + Javascript

Even mixing them is an option, just install the corresponding renderer with npm.
I will be exploring this through small demo _islands_ in upcoming posts.
