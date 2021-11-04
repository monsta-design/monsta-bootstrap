---
layout: docs
title: Vertical rule
description: Use the custom vertical rule helper to create vertical dividers like the `<hr>` element.
group: helpers
toc: true
---

## How it works

Vertical rules are inspired by the `<hr>` element, allowing you to create vertical dividers in common layouts. They're styled just like `<hr>` elements:

- They're `1px` wide
- They have `min-height` of `1em`
- Their color is set via `currentColor` and `opacity`

Customize them with additional styles as needed.

## Example

{{< example >}}
<div class="bs-vr"></div>
{{< /example >}}

Vertical rules scale their height in flex layouts:

{{< example >}}
<div class="bs-d-flex" style="height: 200px;">
  <div class="bs-vr"></div>
</div>
{{< /example >}}

## With stacks

They can also be used in [stacks]({{< docsref "/helpers/stacks" >}}):

{{< example >}}
<div class="bs-hstack bs-gap-3">
  <div class="bs-bg-light bs-border">First item</div>
  <div class="bs-bg-light bs-border bs-ms-auto">Second item</div>
  <div class="bs-vr"></div>
  <div class="bs-bg-light bs-border">Third item</div>
</div>
{{< /example >}}
