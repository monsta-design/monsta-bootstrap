---
layout: docs
title: Gutters
description: Gutters are the padding between your columns, used to responsively space and align content in the Bootstrap grid system.
group: layout
toc: true
---

## How they work

- **Gutters are the gaps between column content, created by horizontal `padding`.** We set `padding-right` and `padding-left` on each column, and use negative `margin` to offset that at the start and end of each row to align content.

- **Gutters start at `1.5rem` (`24px`) wide.** This allows us to match our grid to the [padding and margin spacers]({{< docsref "/utilities/spacing" >}}) scale.

- **Gutters can be responsively adjusted.** Use breakpoint-specific gutter classes to modify horizontal gutters, vertical gutters, and all gutters.

## Horizontal gutters

`.gx-*` classes can be used to control the horizontal gutter widths. The `.container` or `.container-fluid` parent may need to be adjusted if larger gutters are used too to avoid unwanted overflow, using a matching padding utility. For example, in the following example we've increased the padding with `.px-4`:

{{< example >}}
<div class="bs-container bs-px-4">
  <div class="bs-row bs-gx-5">
    <div class="bs-col">
     <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
  </div>
</div>
{{< /example >}}

An alternative solution is to add a wrapper around the `.row` with the `.overflow-hidden` class:

{{< example >}}
<div class="bs-container bs-overflow-hidden">
  <div class="bs-row bs-gx-5">
    <div class="bs-col">
     <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
  </div>
</div>
{{< /example >}}

## Vertical gutters

`.gy-*` classes can be used to control the vertical gutter widths. Like the horizontal gutters, the vertical gutters can cause some overflow below the `.row` at the end of a page. If this occurs, you add a wrapper around `.row` with the `.overflow-hidden` class:

{{< example >}}
<div class="bs-container bs-overflow-hidden">
  <div class="bs-row bs-gy-5">
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
  </div>
</div>
{{< /example >}}

## Horizontal & vertical gutters

`.g-*` classes can be used to control the horizontal gutter widths, for the following example we use a smaller gutter width, so there won't be a need to add the `.overflow-hidden` wrapper class.

{{< example >}}
<div class="bs-container">
  <div class="bs-row bs-g-2">
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
    <div class="bs-col-6">
      <div class="bs-p-3 bs-border bs-bg-light">Custom column padding</div>
    </div>
  </div>
</div>
{{< /example >}}

## Row columns gutters

Gutter classes can also be added to [row columns]({{< docsref "/layout/grid#row-columns" >}}). In the following example, we use responsive row columns and responsive gutter classes.

{{< example >}}
<div class="bs-container">
  <div class="bs-row bs-row-cols-2 bs-row-cols-lg-5 bs-g-2 bs-g-lg-3">
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
    <div class="bs-col">
      <div class="bs-p-3 bs-border bs-bg-light">Row column</div>
    </div>
  </div>
</div>
{{< /example >}}

## No gutters

The gutters between columns in our predefined grid classes can be removed with `.g-0`. This removes the negative `margin`s from `.row` and the horizontal `padding` from all immediate children columns.

**Need an edge-to-edge design?** Drop the parent `.container` or `.container-fluid`.

In practice, here's how it looks. Note you can continue to use this with all other predefined grid classes (including column widths, responsive tiers, reorders, and more).

{{< example class="bd-example-row" >}}
<div class="bs-row bs-g-0">
  <div class="bs-col-sm-6 bs-col-md-8">.bs-col-sm-6 .bs-col-md-8</div>
  <div class="bs-col-6 bs-col-md-4">.bs-col-6 .bs-col-md-4</div>
</div>
{{< /example >}}

## Change the gutters

Classes are built from the `$gutters` Sass map which is inherited from the `$spacers` Sass map.

```scss
$grid-gutter-width: 1.5rem;
$gutters: (
  0: 0,
  1: $spacer * .25,
  2: $spacer * .5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
);
```
