---
layout: docs
title: Input group
description: Easily extend form controls by adding text, buttons, or button groups on either side of textual inputs, custom selects, and custom file inputs.
group: forms
toc: true
---

## Basic example

Place one add-on or button on either side of an input. You may also place one on both sides of an input. Remember to place `<label>`s outside the input group.

{{< example >}}
<div class="bs-input-group mb-3">
  <span class="bs-input-group-text" id="basic-addon1">@</span>
  <input type="text" class="bs-form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
</div>

<div class="bs-input-group mb-3">
  <input type="text" class="bs-form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2">
  <span class="bs-input-group-text" id="basic-addon2">@example.com</span>
</div>

<label for="basic-url" class="bs-form-label">Your vanity URL</label>
<div class="bs-input-group mb-3">
  <span class="bs-input-group-text" id="basic-addon3">https://example.com/users/</span>
  <input type="text" class="bs-form-control" id="basic-url" aria-describedby="basic-addon3">
</div>

<div class="bs-input-group mb-3">
  <span class="bs-input-group-text">$</span>
  <input type="text" class="bs-form-control" aria-label="Amount (to the nearest dollar)">
  <span class="bs-input-group-text">.00</span>
</div>

<div class="bs-input-group mb-3">
  <input type="text" class="bs-form-control" placeholder="Username" aria-label="Username">
  <span class="bs-input-group-text">@</span>
  <input type="text" class="bs-form-control" placeholder="Server" aria-label="Server">
</div>

<div class="bs-input-group">
  <span class="bs-input-group-text">With textarea</span>
  <textarea class="bs-form-control" aria-label="With textarea"></textarea>
</div>
{{< /example >}}

## Wrapping

Input groups wrap by default via `flex-wrap: wrap` in order to accommodate custom form field validation within an input group. You may disable this with `.flex-nowrap`.

{{< example >}}
<div class="bs-input-group flex-nowrap">
  <span class="bs-input-group-text" id="addon-wrapping">@</span>
  <input type="text" class="bs-form-control" placeholder="Username" aria-label="Username" aria-describedby="addon-wrapping">
</div>
{{< /example >}}

## Sizing

Add the relative form sizing classes to the `.input-group` itself and contents within will automatically resize—no need for repeating the form control size classes on each element.

**Sizing on the individual input group elements isn't supported.**

{{< example >}}
<div class="bs-input-group input-group-sm mb-3">
  <span class="bs-input-group-text" id="inputGroup-sizing-sm">Small</span>
  <input type="text" class="bs-form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-sm">
</div>

<div class="bs-input-group bs-mb-3">
  <span class="bs-input-group-text" id="inputGroup-sizing-default">Default</span>
  <input type="text" class="bs-form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-default">
</div>

<div class="bs-input-group input-group-lg">
  <span class="bs-input-group-text" id="inputGroup-sizing-lg">Large</span>
  <input type="text" class="bs-form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-lg">
</div>
{{< /example >}}

## Checkboxes and radios

Place any checkbox or radio option within an input group's addon instead of text. We recommend adding `.mt-0` to the `.form-check-input` when there's no visible text next to the input.

{{< example >}}
<div class="bs-input-group bs-mb-3">
  <div class="bs-input-group-text">
    <input class="bs-form-check-input bs-mt-0" type="checkbox" value="" aria-label="Checkbox for following text input">
  </div>
  <input type="text" class="bs-form-control" aria-label="Text input with checkbox">
</div>

<div class="bs-input-group">
  <div class="bs-input-group-text">
    <input class="bs-form-check-input bs-mt-0" type="radio" value="" aria-label="Radio button for following text input">
  </div>
  <input type="text" class="bs-form-control" aria-label="Text input with radio button">
</div>
{{< /example >}}

## Multiple inputs

While multiple `<input>`s are supported visually, validation styles are only available for input groups with a single `<input>`.

{{< example >}}
<div class="bs-input-group">
  <span class="bs-input-group-text">First and last name</span>
  <input type="text" aria-label="First name" class="bs-form-control">
  <input type="text" aria-label="Last name" class="bs-form-control">
</div>
{{< /example >}}

## Multiple addons

Multiple add-ons are supported and can be mixed with checkbox and radio input versions.

{{< example >}}
<div class="bs-input-group mb-3">
  <span class="bs-input-group-text">$</span>
  <span class="bs-input-group-text">0.00</span>
  <input type="text" class="bs-form-control" aria-label="Dollar amount (with dot and two decimal places)">
</div>

<div class="bs-input-group">
  <input type="text" class="bs-form-control" aria-label="Dollar amount (with dot and two decimal places)">
  <span class="bs-input-group-text">$</span>
  <span class="bs-input-group-text">0.00</span>
</div>
{{< /example >}}

## Button addons

{{< example >}}
<div class="bs-input-group bs-mb-3">
  <button class="bs-btn bs-btn-outline-secondary" type="button" id="button-addon1">Button</button>
  <input type="text" class="bs-form-control" placeholder="" aria-label="Example text with button addon" aria-describedby="button-addon1">
</div>

<div class="bs-input-group bs-mb-3">
  <input type="text" class="bs-form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="button-addon2">
  <button class="bs-btn bs-btn-outline-secondary" type="button" id="button-addon2">Button</button>
</div>

<div class="bs-input-group bs-mb-3">
  <button class="bs-btn bs-btn-outline-secondary" type="button">Button</button>
  <button class="bs-btn bs-btn-outline-secondary" type="button">Button</button>
  <input type="text" class="bs-form-control" placeholder="" aria-label="Example text with two button addons">
</div>

<div class="bs-input-group">
  <input type="text" class="bs-form-control" placeholder="Recipient's username" aria-label="Recipient's username with two button addons">
  <button class="bs-btn bs-btn-outline-secondary" type="button">Button</button>
  <button class="bs-btn bs-btn-outline-secondary" type="button">Button</button>
</div>
{{< /example >}}

## Buttons with dropdowns

{{< example >}}
<div class="bs-input-group bs-mb-3">
  <button class="bs-btn bs-btn-outline-secondary bs-dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">Dropdown</button>
  <ul class="bs-dropdown-menu">
    <li><a class="bs-dropdown-item" href="#">Action</a></li>
    <li><a class="bs-dropdown-item" href="#">Another action</a></li>
    <li><a class="bs-dropdown-item" href="#">Something else here</a></li>
    <li><hr class="bs-dropdown-divider"></li>
    <li><a class="bs-dropdown-item" href="#">Separated link</a></li>
  </ul>
  <input type="text" class="bs-form-control" aria-label="Text input with dropdown button">
</div>

<div class="bs-input-group bs-mb-3">
  <input type="text" class="bs-form-control" aria-label="Text input with dropdown button">
  <button class="bs-btn bs-btn-outline-secondary bs-dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">Dropdown</button>
  <ul class="bs-dropdown-menu bs-dropdown-menu-end">
    <li><a class="bs-dropdown-item" href="#">Action</a></li>
    <li><a class="bs-dropdown-item" href="#">Another action</a></li>
    <li><a class="bs-dropdown-item" href="#">Something else here</a></li>
    <li><hr class="bs-dropdown-divider"></li>
    <li><a class="bs-dropdown-item" href="#">Separated link</a></li>
  </ul>
</div>

<div class="bs-input-group">
  <button class="bs-btn bs-btn-outline-secondary bs-dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">Dropdown</button>
  <ul class="bs-dropdown-menu">
    <li><a class="bs-dropdown-item" href="#">Action before</a></li>
    <li><a class="bs-dropdown-item" href="#">Another action before</a></li>
    <li><a class="bs-dropdown-item" href="#">Something else here</a></li>
    <li><hr class="bs-dropdown-divider"></li>
    <li><a class="bs-dropdown-item" href="#">Separated link</a></li>
  </ul>
  <input type="text" class="bs-form-control" aria-label="Text input with 2 dropdown buttons">
  <button class="bs-btn bs-btn-outline-secondary bs-dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">Dropdown</button>
  <ul class="bs-dropdown-menu bs-dropdown-menu-end">
    <li><a class="bs-dropdown-item" href="#">Action</a></li>
    <li><a class="bs-dropdown-item" href="#">Another action</a></li>
    <li><a class="bs-dropdown-item" href="#">Something else here</a></li>
    <li><hr class="bs-dropdown-divider"></li>
    <li><a class="bs-dropdown-item" href="#">Separated link</a></li>
  </ul>
</div>
{{< /example >}}

## Segmented buttons

{{< example >}}
<div class="bs-input-group mb-3">
  <button type="button" class="bs-btn bs-btn-outline-secondary">Action</button>
  <button type="button" class="bs-btn bs-btn-outline-secondary dropdown-toggle dropdown-toggle-split" data-bs-toggle="dropdown" aria-expanded="false">
    <span class="bs-visually-hidden">Toggle Dropdown</span>
  </button>
  <ul class="bs-dropdown-menu">
    <li><a class="bs-dropdown-item" href="#">Action</a></li>
    <li><a class="bs-dropdown-item" href="#">Another action</a></li>
    <li><a class="bs-dropdown-item" href="#">Something else here</a></li>
    <li><hr class="bs-dropdown-divider"></li>
    <li><a class="bs-dropdown-item" href="#">Separated link</a></li>
  </ul>
  <input type="text" class="bs-form-control" aria-label="Text input with segmented dropdown button">
</div>

<div class="bs-input-group">
  <input type="text" class="bs-form-control" aria-label="Text input with segmented dropdown button">
  <button type="button" class="bs-btn btn-outline-secondary">Action</button>
  <button type="button" class="bs-btn btn-outline-secondary dropdown-toggle dropdown-toggle-split" data-bs-toggle="dropdown" aria-expanded="false">
    <span class="bs-visually-hidden">Toggle Dropdown</span>
  </button>
  <ul class="bs-dropdown-menu bs-dropdown-menu-end">
    <li><a class="bs-dropdown-item" href="#">Action</a></li>
    <li><a class="bs-dropdown-item" href="#">Another action</a></li>
    <li><a class="bs-dropdown-item" href="#">Something else here</a></li>
    <li><hr class="bs-dropdown-divider"></li>
    <li><a class="bs-dropdown-item" href="#">Separated link</a></li>
  </ul>
</div>
{{< /example >}}

## Custom forms

Input groups include support for custom selects and custom file inputs. Browser default versions of these are not supported.

### Custom select

{{< example >}}
<div class="bs-input-group mb-3">
  <label class="bs-input-group-text" for="inputGroupSelect01">Options</label>
  <select class="bs-form-select" id="inputGroupSelect01">
    <option selected>Choose...</option>
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
  </select>
</div>

<div class="bs-input-group bs-mb-3">
  <select class="bs-form-select" id="inputGroupSelect02">
    <option selected>Choose...</option>
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
  </select>
  <label class="bs-input-group-text" for="inputGroupSelect02">Options</label>
</div>

<div class="bs-input-group bs-mb-3">
  <button class="bs-btn bs-btn-outline-secondary" type="button">Button</button>
  <select class="bs-form-select" id="inputGroupSelect03" aria-label="Example select with button addon">
    <option selected>Choose...</option>
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
  </select>
</div>

<div class="bs-input-group">
  <select class="bs-form-select" id="inputGroupSelect04" aria-label="Example select with button addon">
    <option selected>Choose...</option>
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
  </select>
  <button class="bs-btn bs-btn-outline-secondary" type="button">Button</button>
</div>
{{< /example >}}

### Custom file input

{{< example >}}
<div class="bs-input-group mb-3">
  <label class="bs-input-group-text" for="inputGroupFile01">Upload</label>
  <input type="file" class="bs-form-control" id="inputGroupFile01">
</div>

<div class="bs-input-group mb-3">
  <input type="file" class="bs-form-control" id="inputGroupFile02">
  <label class="bs-input-group-text" for="inputGroupFile02">Upload</label>
</div>

<div class="bs-input-group mb-3">
  <button class="bs-btn bs-btn-outline-secondary" type="button" id="inputGroupFileAddon03">Button</button>
  <input type="file" class="bs-form-control" id="inputGroupFile03" aria-describedby="inputGroupFileAddon03" aria-label="Upload">
</div>

<div class="bs-input-group">
  <input type="file" class="bs-form-control" id="inputGroupFile04" aria-describedby="inputGroupFileAddon04" aria-label="Upload">
  <button class="bs-btn bs-btn-outline-secondary" type="button" id="inputGroupFileAddon04">Button</button>
</div>
{{< /example >}}

## Sass

### Variables

{{< scss-docs name="input-group-variables" file="scss/_variables.scss" >}}
