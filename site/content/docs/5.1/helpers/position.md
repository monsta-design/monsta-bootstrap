---
layout: docs
title: Position
description: Use these helpers for quickly configuring the position of an element.
group: helpers
toc: true
---

## Fixed top

Position an element at the top of the viewport, from edge to edge. Be sure you understand the ramifications of fixed position in your project; you may need to add additional CSS.

```html
<div class="bs-fixed-top">...</div>
```

## Fixed bottom

Position an element at the bottom of the viewport, from edge to edge. Be sure you understand the ramifications of fixed position in your project; you may need to add additional CSS.

```html
<div class="bs-fixed-bottom">...</div>
```

## Sticky top

Position an element at the top of the viewport, from edge to edge, but only after you scroll past it. The `.sticky-top` utility uses CSS's `position: sticky`, which isn't fully supported in all browsers.

```html
<div class="bs-sticky-top">...</div>
```

## Responsive sticky top

Responsive variations also exist for `.sticky-top` utility.

```html
<div class="bs-sticky-sm-top">Stick to the top on viewports sized SM (small) or wider</div>
<div class="bs-sticky-md-top">Stick to the top on viewports sized MD (medium) or wider</div>
<div class="bs-sticky-lg-top">Stick to the top on viewports sized LG (large) or wider</div>
<div class="bs-sticky-xl-top">Stick to the top on viewports sized XL (extra-large) or wider</div>
```
