---
layout: docs
title: Cards
description: Bootstrap's cards provide a flexible and extensible content container with multiple variants and options.
group: components
toc: true
---

## About

A **card** is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options. If you're familiar with Bootstrap 3, cards replace our old panels, wells, and thumbnails. Similar functionality to those components is available as modifier classes for cards.

## Example

Cards are built with as little markup and styles as possible, but still manage to deliver a ton of control and customization. Built with flexbox, they offer easy alignment and mix well with other Bootstrap components. They have no `margin` by default, so use [spacing utilities]({{< docsref "/utilities/spacing" >}}) as needed.

Below is an example of a basic card with mixed content and a fixed width. Cards have no fixed width to start, so they'll naturally fill the full width of its parent element. This is easily customized with our various [sizing options](#sizing).

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

## Content types

Cards support a wide variety of content, including images, text, list groups, links, and more. Below are examples of what's supported.

### Body

The building block of a card is the `.card-body`. Use it whenever you need a padded section within a card.

{{< example >}}
<div class="bs-card">
  <div class="bs-card-body">
    This is some text within a card body.
  </div>
</div>
{{< /example >}}

### Titles, text, and links

Card titles are used by adding `.card-title` to a `<h*>` tag. In the same way, links are added and placed next to each other by adding `.card-link` to an `<a>` tag.

Subtitles are used by adding a `.card-subtitle` to a `<h*>` tag. If the `.card-title` and the `.card-subtitle` items are placed in a `.card-body` item, the card title and subtitle are aligned nicely.

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <h6 class="bs-card-subtitle bs-mb-2 bs-text-muted">Card subtitle</h6>
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="bs-card-link">Card link</a>
    <a href="#" class="bs-card-link">Another link</a>
  </div>
</div>
{{< /example >}}

### Images

`.card-img-top` places an image to the top of the card. With `.card-text`, text can be added to the card. Text within `.card-text` can also be styled with the standard HTML tags.

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
  <div class="bs-card-body">
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
{{< /example >}}

### List groups

Create lists of content in a card with a flush list group.

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  <ul class="bs-list-group list-group-flush">
    <li class="bs-list-group-item">An item</li>
    <li class="bs-list-group-item">A second item</li>
    <li class="bs-list-group-item">A third item</li>
  </ul>
</div>
{{< /example >}}

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  <div class="bs-card-header">
    Featured
  </div>
  <ul class="bs-list-group list-group-flush">
    <li class="bs-list-group-item">An item</li>
    <li class="bs-list-group-item">A second item</li>
    <li class="bs-list-group-item">A third item</li>
  </ul>
</div>
{{< /example >}}

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  <ul class="bs-list-group list-group-flush">
    <li class="bs-list-group-item">An item</li>
    <li class="bs-list-group-item">A second item</li>
    <li class="bs-list-group-item">A third item</li>
  </ul>
  <div class="bs-card-footer">
    Card footer
  </div>
</div>
{{< /example >}}

### Kitchen sink

Mix and match multiple content types to create the card you need, or throw everything in there. Shown below are image styles, blocks, text styles, and a list group—all wrapped in a fixed-width card.

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
  <ul class="bs-list-group list-group-flush">
    <li class="bs-list-group-item">An item</li>
    <li class="bs-list-group-item">A second item</li>
    <li class="bs-list-group-item">A third item</li>
  </ul>
  <div class="bs-card-body">
    <a href="#" class="bs-card-link">Card link</a>
    <a href="#" class="bs-card-link">Another link</a>
  </div>
</div>
{{< /example >}}

### Header and footer

Add an optional header and/or footer within a card.

{{< example >}}
<div class="bs-card">
  <div class="bs-card-header">
    Featured
  </div>
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

Card headers can be styled by adding `.card-header` to `<h*>` elements.

{{< example >}}
<div class="bs-card">
  <h5 class="bs-card-header">Featured</h5>
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

{{< example >}}
<div class="bs-card">
  <div class="bs-card-header">
    Quote
  </div>
  <div class="bs-card-body">
    <blockquote class="bs-blockquote bs-mb-0">
      <p>A well-known quote, contained in a blockquote element.</p>
      <footer class="bs-blockquote-footer">Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
{{< /example >}}

{{< example >}}
<div class="bs-card bs-text-center">
  <div class="card-header">
    Featured
  </div>
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
  <div class="bs-card-footer bs-text-muted">
    2 days ago
  </div>
</div>
{{< /example >}}

## Sizing

Cards assume no specific `width` to start, so they'll be 100% wide unless otherwise stated. You can change this as needed with custom CSS, grid classes, grid Sass mixins, or utilities.

### Using grid markup

Using the grid, wrap cards in columns and rows as needed.

{{< example >}}
<div class="bs-row">
  <div class="bs-col-sm-6">
    <div class="bs-card">
      <div class="bs-card-body">
        <h5 class="bs-card-title">Special title treatment</h5>
        <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
        <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
      </div>
    </div>
  </div>
  <div class="bs-col-sm-6">
    <div class="bs-card">
      <div class="bs-card-body">
        <h5 class="bs-card-title">Special title treatment</h5>
        <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
        <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
      </div>
    </div>
  </div>
</div>
{{< /example >}}

### Using utilities

Use our handful of [available sizing utilities]({{< docsref "/utilities/sizing" >}}) to quickly set a card's width.

{{< example >}}
<div class="bs-card w-75">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Button</a>
  </div>
</div>

<div class="bs-card bs-w-50">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Button</a>
  </div>
</div>
{{< /example >}}

### Using custom CSS

Use custom CSS in your stylesheets or as inline styles to set a width.

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

## Text alignment

You can quickly change the text alignment of any card—in its entirety or specific parts—with our [text align classes]({{< docsref "/utilities/text#text-alignment" >}}).

{{< example >}}
<div class="bs-card" style="width: 18rem;">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>

<div class="bs-card bs-text-center" style="width: 18rem;">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>

<div class="card text-end" style="width: 18rem;">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

## Navigation

Add some navigation to a card's header (or block) with Bootstrap's [nav components]({{< docsref "/components/navs-tabs" >}}).

{{< example >}}
<div class="bs-card text-center">
  <div class="bs-card-header">
    <ul class="bs-nav bs-nav-tabs card-header-tabs">
      <li class="bs-nav-item">
        <a class="bs-nav-link bs-active" aria-current="true" href="#">Active</a>
      </li>
      <li class="bs-nav-item">
        <a class="bs-nav-link" href="#">Link</a>
      </li>
      <li class="bs-nav-item">
        <a class="bs-nav-link bs-disabled">Disabled</a>
      </li>
    </ul>
  </div>
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

{{< example >}}
<div class="bs-card bs-text-center">
  <div class="bs-card-header">
    <ul class="bs-nav bs-nav-pills bs-card-header-pills">
      <li class="bs-nav-item">
        <a class="bs-nav-link bs-active" href="#">Active</a>
      </li>
      <li class="bs-nav-item">
        <a class="bs-nav-link" href="#">Link</a>
      </li>
      <li class="bs-nav-item">
        <a class="bs-nav-link disabled">Disabled</a>
      </li>
    </ul>
  </div>
  <div class="bs-card-body">
    <h5 class="bs-card-title">Special title treatment</h5>
    <p class="bs-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="bs-btn bs-btn-primary">Go somewhere</a>
  </div>
</div>
{{< /example >}}

## Images

Cards include a few options for working with images. Choose from appending "image caps" at either end of a card, overlaying images with card content, or simply embedding the image in a card.

### Image caps

Similar to headers and footers, cards can include top and bottom "image caps"—images at the top or bottom of a card.

{{< example >}}
<div class="bs-card bs-mb-3">
  {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="bs-card-text"><small class="bs-text-muted">Last updated 3 mins ago</small></p>
  </div>
</div>
<div class="bs-card">
  <div class="bs-card-body">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="bs-card-text"><small class="bs-text-muted">Last updated 3 mins ago</small></p>
  </div>
  {{< placeholder width="100%" height="180" class="bs-card-img-bottom" text="Image cap" >}}
</div>
{{< /example >}}

### Image overlays

Turn an image into a card background and overlay your card's text. Depending on the image, you may or may not need additional styles or utilities.

{{< example >}}
<div class="bs-card bs-bg-dark bs-text-white">
  {{< placeholder width="100%" height="270" class="bs-bd-placeholder-img-lg card-img" text="Card image" >}}
  <div class="bs-card-img-overlay">
    <h5 class="bs-card-title">Card title</h5>
    <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="bs-card-text">Last updated 3 mins ago</p>
  </div>
</div>
{{< /example >}}

{{< callout info >}}
Note that content should not be larger than the height of the image. If content is larger than the image the content will be displayed outside the image.
{{< /callout >}}

## Horizontal

Using a combination of grid and utility classes, cards can be made horizontal in a mobile-friendly and responsive way. In the example below, we remove the grid gutters with `.g-0` and use `.col-md-*` classes to make the card horizontal at the `md` breakpoint. Further adjustments may be needed depending on your card content.

{{< example >}}
<div class="bs-card bs-mb-3" style="max-width: 540px;">
  <div class="bs-row bs-g-0">
    <div class="bs-col-md-4">
      {{< placeholder width="100%" height="250" text="Image" class="bs-img-fluid rounded-start" >}}
    </div>
    <div class="bs-col-md-8">
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
        <p class="bs-card-text"><small class="bs-text-muted">Last updated 3 mins ago</small></p>
      </div>
    </div>
  </div>
</div>
{{< /example >}}

## Card styles

Cards include various options for customizing their backgrounds, borders, and color.

### Background and color

Use [text color]({{< docsref "/utilities/colors" >}}) and [background utilities]({{< docsref "/utilities/background" >}}) to change the appearance of a card.

{{< example >}}
{{< card.inline >}}
{{- range (index $.Site.Data "theme-colors") }}
<div class="bs-card{{ if .contrast_color }} text-{{ .contrast_color }}{{ else }} text-white{{ end }} bg-{{ .name }} mb-3" style="max-width: 18rem;">
  <div class="bs-card-header">Header</div>
  <div class="bs-card-body">
    <h5 class="bs-card-title">{{ .name | title }} card title</h5>
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
{{- end -}}
{{< /card.inline >}}
{{< /example >}}

{{< callout info >}}
{{< partial "callout-warning-color-assistive-technologies.md" >}}
{{< /callout >}}

### Border

Use [border utilities]({{< docsref "/utilities/borders" >}}) to change just the `border-color` of a card. Note that you can put `.text-{color}` classes on the parent `.card` or a subset of the card's contents as shown below.

{{< example >}}
{{< card.inline >}}
{{- range (index $.Site.Data "theme-colors") }}
<div class="bs-card bs-border-{{ .name }} mb-3" style="max-width: 18rem;">
  <div class="bs-card-header">Header</div>
  <div class="bs-card-body{{ if not .contrast_color }} text-{{ .name }}{{ end }}">
    <h5 class="bs-card-title">{{ .name | title }} card title</h5>
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
{{- end -}}
{{< /card.inline >}}
{{< /example >}}

### Mixins utilities

You can also change the borders on the card header and footer as needed, and even remove their `background-color` with `.bg-transparent`.

{{< example >}}
<div class="bs-card border-success mb-3" style="max-width: 18rem;">
  <div class="bs-card-header bg-transparent border-success">Header</div>
  <div class="bs-card-body text-success">
    <h5 class="bs-card-title">Success card title</h5>
    <p class="bs-card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
  <div class="bs-card-footer bg-transparent border-success">Footer</div>
</div>
{{< /example >}}

## Card layout

In addition to styling the content within cards, Bootstrap includes a few options for laying out series of cards. For the time being, **these layout options are not yet responsive**.

### Card groups

Use card groups to render cards as a single, attached element with equal width and height columns. Card groups start off stacked and use `display: flex;` to become attached with uniform dimensions starting at the `sm` breakpoint.

{{< example >}}
<div class="bs-card-group">
  <div class="bs-card">
    {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
    <div class="bs-card-body">
      <h5 class="bs-card-title">Card title</h5>
      <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      <p class="bs-card-text"><small class="bs-text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="bs-card">
    {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
    <div class="bs-card-body">
      <h5 class="bs-card-title">Card title</h5>
      <p class="bs-card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="bs-card-text"><small class="bs-text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="bs-card">
    {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
    <div class="bs-card-body">
      <h5 class="bs-card-title">Card title</h5>
      <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
      <p class="bs-card-text"><small class="bs-text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
</div>
{{< /example >}}

When using card groups with footers, their content will automatically line up.

{{< example >}}
<div class="bs-card-group">
  <div class="bs-card">
    {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
    <div class="bs-card-body">
      <h5 class="bs-card-title">Card title</h5>
      <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    </div>
    <div class="bs-card-footer">
      <small class="bs-text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="bs-card">
    {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
    <div class="bs-card-body">
      <h5 class="bs-card-title">Card title</h5>
      <p class="bs-card-text">This card has supporting text below as a natural lead-in to additional content.</p>
    </div>
    <div class="bs-card-footer">
      <small class="bs-text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="bs-card">
    {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
    <div class="bs-card-body">
      <h5 class="bs-card-title">Card title</h5>
      <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
    </div>
    <div class="bs-card-footer">
      <small class="bs-text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
</div>
{{< /example >}}

### Grid cards

Use the Bootstrap grid system and its [`.row-cols` classes]({{< docsref "/layout/grid#row-columns" >}}) to control how many grid columns (wrapped around your cards) you show per row. For example, here's `.row-cols-1` laying out the cards on one column, and `.row-cols-md-2` splitting four cards to equal width across multiple rows, from the medium breakpoint up.

{{< example >}}
<div class="bs-row row-cols-1 row-cols-md-2 g-4">
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
</div>
{{< /example >}}

Change it to `.row-cols-3` and you'll see the fourth card wrap.

{{< example >}}
<div class="bs-row bs-row-cols-1 bs-row-cols-md-3 bs-g-4">
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
</div>
{{< /example >}}

When you need equal height, add `.h-100` to the cards. If you want equal heights by default, you can set `$card-height: 100%` in Sass.

{{< example >}}
<div class="bs-row bs-row-cols-1 bs-row-cols-md-3 bs-g-4">
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a short card.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content.</p>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="140" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
</div>
{{< /example >}}

Just like with card groups, card footers will automatically line up.

{{< example >}}
<div class="bs-row bs-row-cols-1 bs-row-cols-md-3 bs-g-4">
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
      <div class="bs-card-footer">
        <small class="bs-text-muted">Last updated 3 mins ago</small>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      </div>
      <div class="bs-card-footer">
        <small class="bs-text-muted">Last updated 3 mins ago</small>
      </div>
    </div>
  </div>
  <div class="bs-col">
    <div class="bs-card bs-h-100">
      {{< placeholder width="100%" height="180" class="bs-card-img-top" text="Image cap" >}}
      <div class="bs-card-body">
        <h5 class="bs-card-title">Card title</h5>
        <p class="bs-card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
      </div>
      <div class="bs-card-footer">
        <small class="bs-text-muted">Last updated 3 mins ago</small>
      </div>
    </div>
  </div>
</div>
{{< /example >}}

### Masonry

In `v4` we used a CSS-only technique to mimic the behavior of [Masonry](https://masonry.desandro.com/)-like columns, but this technique came with lots of unpleasant [side effects](https://github.com/twbs/bootstrap/pull/28922). If you want to have this type of layout in `v5`, you can just make use of Masonry plugin. **Masonry is not included in Bootstrap**, but we've made a [demo example]({{< docsref "/examples/masonry" >}}) to help you get started.

## Sass

### Variables

{{< scss-docs name="card-variables" file="scss/_variables.scss" >}}
