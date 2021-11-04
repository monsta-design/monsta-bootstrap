---
layout: docs
title: Stacks
description: Shorthand helpers that build on top of our flexbox utilities to make component layout faster and easier than ever.
group: helpers
toc: true
---

Stacks offer a shortcut for applying a number of flexbox properties to quickly and easily create layouts in Bootstrap. All credit for the concept and implementation goes to the open source [Pylon project](https://almonk.github.io/pylon/).

{{< callout warning >}}
Heads up! Support for gap utilities with flexbox was recently added to Safari, so consider verifying your intended browser support. Grid layout should have no issues. [Read more](https://caniuse.com/flexbox-gap).
{{< /callout >}}

## Vertical

Use `.vstack` to create vertical layouts. Stacked items are full-width by default. Use `.gap-*` utilities to add space between items.

{{< example >}}
<div class="bs-vstack bs-gap-3">
  <div class="bs-bg-light bs-border">First item</div>
  <div class="bs-bg-light bs-border">Second item</div>
  <div class="bs-bg-light bs-border">Third item</div>
</div>
{{< /example >}}

## Horizontal

Use `.hstack` for horizontal layouts. Stacked items are vertically centered by default and only take up their necessary width. Use `.gap-*` utilities to add space between items.

{{< example >}}
<div class="bs-hstack bs-gap-3">
  <div class="bs-bg-light bs-border">First item</div>
  <div class="bs-bg-light bs-border">Second item</div>
  <div class="bs-bg-light bs-border">Third item</div>
</div>
{{< /example >}}

Using horizontal margin utilities like `.ms-auto` as spacers:

{{< example >}}
<div class="bs-hstack bs-gap-3">
  <div class="bs-bg-light bs-border">First item</div>
  <div class="bs-bg-light bs-border bs-ms-auto">Second item</div>
  <div class="bs-bg-light bs-border">Third item</div>
</div>
{{< /example >}}

And with [vertical rules]({{< docsref "/helpers/vertical-rule" >}}):

{{< example >}}
<div class="bs-hstack bs-gap-3">
  <div class="bs-bg-light bs-border">First item</div>
  <div class="bs-bg-light bs-border bs-ms-auto">Second item</div>
  <div class="bs-vr"></div>
  <div class="bs-bg-light bs-border">Third item</div>
</div>
{{< /example >}}

## Examples

Use `.vstack` to stack buttons and other elements:

{{< example >}}
<div class="bs-vstack bs-gap-2 bs-col-md-5 bs-mx-auto">
  <button type="button" class="bs-btn bs-btn-secondary">Save changes</button>
  <button type="button" class="bs-btn bs-btn-outline-secondary">Cancel</button>
</div>
{{< /example >}}

Create an inline form with `.hstack`:

{{< example >}}
<div class="bs-hstack bs-gap-3">
  <input class="bs-form-control bs-me-auto" type="text" placeholder="Add your item here..." aria-label="Add your item here...">
  <button type="button" class="bs-btn bs-btn-secondary">Submit</button>
  <div class="bs-vr"></div>
  <button type="button" class="bs-btn bs-btn-outline-danger">Reset</button>
</div>
{{< /example >}}

## Sass

{{< scss-docs name="stacks" file="scss/helpers/_stacks.scss" >}}
