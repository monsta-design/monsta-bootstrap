---
layout: docs
title: Form controls
description: Give textual form controls like `<input>`s and `<textarea>`s an upgrade with custom styles, sizing, focus states, and more.
group: forms
toc: true
---

## Example

{{< example >}}
<div class="bs-mb-3">
  <label for="exampleFormControlInput1" class="bs-form-label">Email address</label>
  <input type="email" class="bs-form-control" id="exampleFormControlInput1" placeholder="name@example.com">
</div>
<div class="bs-mb-3">
  <label for="exampleFormControlTextarea1" class="bs-form-label">Example textarea</label>
  <textarea class="bs-form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
</div>
{{< /example >}}

## Sizing

Set heights using classes like `.form-control-lg` and `.form-control-sm`.

{{< example >}}
<input class="bs-form-control bs-form-control-lg" type="text" placeholder=".form-control-lg" aria-label=".form-control-lg example">
<input class="bs-form-control" type="text" placeholder="Default input" aria-label="default input example">
<input class="bs-form-control bs-form-control-sm" type="text" placeholder=".form-control-sm" aria-label=".form-control-sm example">
{{< /example >}}

## Disabled

Add the `disabled` boolean attribute on an input to give it a grayed out appearance and remove pointer events.

{{< example >}}
<input class="bs-form-control" type="text" placeholder="Disabled input" aria-label="Disabled input example" disabled>
<input class="bs-form-control" type="text" value="Disabled readonly input" aria-label="Disabled input example" disabled readonly>
{{< /example >}}

## Readonly

Add the `readonly` boolean attribute on an input to prevent modification of the input's value.

{{< example >}}
<input class="bs-form-control" type="text" value="Readonly input here..." aria-label="readonly input example" readonly>
{{< /example >}}

## Readonly plain text

If you want to have `<input readonly>` elements in your form styled as plain text, use the `.form-control-plaintext` class to remove the default form field styling and preserve the correct margin and padding.

{{< example >}}
  <div class="bs-mb-3 bs-row">
    <label for="staticEmail" class="bs-col-sm-2 bs-col-form-label">Email</label>
    <div class="bs-col-sm-10">
      <input type="text" readonly class="bs-form-control-plaintext" id="staticEmail" value="email@example.com">
    </div>
  </div>
  <div class="bs-mb-3 bs-row">
    <label for="inputPassword" class="bs-col-sm-2 bs-col-form-label">Password</label>
    <div class="bs-col-sm-10">
      <input type="password" class="bs-form-control" id="inputPassword">
    </div>
  </div>
{{< /example >}}

{{< example >}}
<form class="bs-row bs-g-3">
  <div class="bs-col-auto">
    <label for="staticEmail2" class="bs-visually-hidden">Email</label>
    <input type="text" readonly class="bs-form-control-plaintext" id="staticEmail2" value="email@example.com">
  </div>
  <div class="bs-col-auto">
    <label for="inputPassword2" class="bs-visually-hidden">Password</label>
    <input type="password" class="bs-form-control" id="inputPassword2" placeholder="Password">
  </div>
  <div class="bs-col-auto">
    <button type="submit" class="bs-btn bs-btn-primary bs-mb-3">Confirm identity</button>
  </div>
</form>
{{< /example >}}

## File input

{{< example >}}
<div class="bs-mb-3">
  <label for="formFile" class="bs-form-label">Default file input example</label>
  <input class="bs-form-control" type="file" id="formFile">
</div>
<div class="bs-mb-3">
  <label for="formFileMultiple" class="bs-form-label">Multiple files input example</label>
  <input class="bs-form-control" type="file" id="formFileMultiple" multiple>
</div>
<div class="bs-mb-3">
  <label for="formFileDisabled" class="bs-form-label">Disabled file input example</label>
  <input class="bs-form-control" type="file" id="formFileDisabled" disabled>
</div>
<div class="bs-mb-3">
  <label for="formFileSm" class="bs-form-label">Small file input example</label>
  <input class="bs-form-control bs-form-control-sm" id="formFileSm" type="file">
</div>
<div>
  <label for="formFileLg" class="bs-form-label">Large file input example</label>
  <input class="bs-form-control bs-form-control-lg" id="formFileLg" type="file">
</div>
{{< /example >}}

## Color

{{< example >}}
<label for="exampleColorInput" class="bs-form-label">Color picker</label>
<input type="color" class="bs-form-control bs-form-control-color" id="exampleColorInput" value="#563d7c" title="Choose your color">
{{< /example >}}

## Datalists

Datalists allow you to create a group of `<option>`s that can be accessed (and autocompleted) from within an `<input>`. These are similar to `<select>` elements, but come with more menu styling limitations and differences. While most browsers and operating systems include some support for `<datalist>` elements, their styling is inconsistent at best.

Learn more about [support for datalist elements](https://caniuse.com/datalist).

{{< example >}}
<label for="exampleDataList" class="bs-form-label">Datalist example</label>
<input class="bs-form-control" list="datalistOptions" id="exampleDataList" placeholder="Type to search...">
<datalist id="datalistOptions">
  <option value="San Francisco">
  <option value="New York">
  <option value="Seattle">
  <option value="Los Angeles">
  <option value="Chicago">
</datalist>
{{< /example >}}

## Sass

### Variables

`$input-*` are shared across most of our form controls (and not buttons).

{{< scss-docs name="form-input-variables" file="scss/_variables.scss" >}}

`$form-label-*` and `$form-text-*` are for our `<label>`s and `.form-text` component.

{{< scss-docs name="form-label-variables" file="scss/_variables.scss" >}}

{{< scss-docs name="form-text-variables" file="scss/_variables.scss" >}}

`$form-file-*` are for file input.

{{< scss-docs name="form-file-variables" file="scss/_variables.scss" >}}
