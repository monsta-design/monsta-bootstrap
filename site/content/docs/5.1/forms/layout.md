---
layout: docs
title: Layout
description: Give your forms some structure—from inline to horizontal to custom grid implementations—with our form layout options.
group: forms
toc: true
---

## Forms

Every group of form fields should reside in a `<form>` element. Bootstrap provides no default styling for the `<form>` element, but there are some powerful browser features that are provided by default.

- New to browser forms? Consider reviewing [the MDN form docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form) for an overview and complete list of available attributes.
- `<button>`s within a `<form>` default to `type="submit"`, so strive to be specific and always include a `type`.
- You can disable every form element within a form with the `disabled` attribute on the `<form>`.

Since Bootstrap applies `display: block` and `width: 100%` to almost all our form controls, forms will by default stack vertically. Additional classes can be used to vary this layout on a per-form basis.

## Utilities

[Margin utilities]({{< docsref "/utilities/spacing" >}}) are the easiest way to add some structure to forms. They provide basic grouping of labels, controls, optional form text, and form validation messaging. We recommend sticking to `margin-bottom` utilities, and using a single direction throughout the form for consistency.

Feel free to build your forms however you like, with `<fieldset>`s, `<div>`s, or nearly any other element.

{{< example >}}
<div class="bs-mb-3">
  <label for="formGroupExampleInput" class="bs-form-label">Example label</label>
  <input type="text" class="bs-form-control" id="formGroupExampleInput" placeholder="Example input placeholder">
</div>
<div class="bs-mb-3">
  <label for="formGroupExampleInput2" class="bs-form-label">Another label</label>
  <input type="text" class="bs-form-control" id="formGroupExampleInput2" placeholder="Another input placeholder">
</div>
{{< /example >}}

## Form grid

More complex forms can be built using our grid classes. Use these for form layouts that require multiple columns, varied widths, and additional alignment options. **Requires the `$enable-grid-classes` Sass variable to be enabled** (on by default).

{{< example >}}
<div class="bs-row">
  <div class="bs-col">
    <input type="text" class="bs-form-control" placeholder="First name" aria-label="First name">
  </div>
  <div class="bs-col">
    <input type="text" class="bs-form-control" placeholder="Last name" aria-label="Last name">
  </div>
</div>
{{< /example >}}

## Gutters

By adding [gutter modifier classes]({{< docsref "/layout/gutters" >}}), you can have control over the gutter width in as well the inline as block direction. **Also requires the `$enable-grid-classes` Sass variable to be enabled** (on by default).

{{< example >}}
<div class="bs-row bs-g-3">
  <div class="bs-col">
    <input type="text" class="bs-form-control" placeholder="First name" aria-label="First name">
  </div>
  <div class="bs-col">
    <input type="text" class="bs-form-control" placeholder="Last name" aria-label="Last name">
  </div>
</div>
{{< /example >}}

More complex layouts can also be created with the grid system.

{{< example >}}
<form class="bs-row bs-g-3">
  <div class="bs-col-md-6">
    <label for="inputEmail4" class="bs-form-label">Email</label>
    <input type="email" class="bs-form-control" id="inputEmail4">
  </div>
  <div class="bs-col-md-6">
    <label for="inputPassword4" class="bs-form-label">Password</label>
    <input type="password" class="bs-form-control" id="inputPassword4">
  </div>
  <div class="bs-col-12">
    <label for="inputAddress" class="bs-form-label">Address</label>
    <input type="text" class="bs-form-control" id="inputAddress" placeholder="1234 Main St">
  </div>
  <div class="bs-col-12">
    <label for="inputAddress2" class="bs-form-label">Address 2</label>
    <input type="text" class="bs-form-control" id="inputAddress2" placeholder="Apartment, studio, or floor">
  </div>
  <div class="bs-col-md-6">
    <label for="inputCity" class="bs-form-label">City</label>
    <input type="text" class="bs-form-control" id="inputCity">
  </div>
  <div class="bs-col-md-4">
    <label for="inputState" class="bs-form-label">State</label>
    <select id="inputState" class="bs-form-select">
      <option selected>Choose...</option>
      <option>...</option>
    </select>
  </div>
  <div class="bs-col-md-2">
    <label for="inputZip" class="bs-form-label">Zip</label>
    <input type="text" class="bs-form-control" id="inputZip">
  </div>
  <div class="bs-col-12">
    <div class="bs-form-check">
      <input class="bs-form-check-input" type="checkbox" id="gridCheck">
      <label class="bs-form-check-label" for="gridCheck">
        Check me out
      </label>
    </div>
  </div>
  <div class="bs-col-12">
    <button type="submit" class="bs-btn bs-btn-primary">Sign in</button>
  </div>
</form>
{{< /example >}}

## Horizontal form

Create horizontal forms with the grid by adding the `.row` class to form groups and using the `.col-*-*` classes to specify the width of your labels and controls. Be sure to add `.col-form-label` to your `<label>`s as well so they're vertically centered with their associated form controls.

At times, you maybe need to use margin or padding utilities to create that perfect alignment you need. For example, we've removed the `padding-top` on our stacked radio inputs label to better align the text baseline.

{{< example >}}
<form>
  <div class="bs-row bs-mb-3">
    <label for="inputEmail3" class="bs-col-sm-2 col-form-label">Email</label>
    <div class="bs-col-sm-10">
      <input type="email" class="bs-form-control" id="inputEmail3">
    </div>
  </div>
  <div class="bs-row bs-mb-3">
    <label for="inputPassword3" class="bs-col-sm-2 bs-col-form-label">Password</label>
    <div class="bs-col-sm-10">
      <input type="password" class="bs-form-control" id="inputPassword3">
    </div>
  </div>
  <fieldset class="bs-row bs-mb-3">
    <legend class="bs-col-form-label bs-col-sm-2 bs-pt-0">Radios</legend>
    <div class="bs-col-sm-10">
      <div class="bs-form-check">
        <input class="bs-form-check-input" type="radio" name="gridRadios" id="gridRadios1" value="option1" checked>
        <label class="bs-form-check-label" for="gridRadios1">
          First radio
        </label>
      </div>
      <div class="bs-form-check">
        <input class="bs-form-check-input" type="radio" name="gridRadios" id="gridRadios2" value="option2">
        <label class="bs-form-check-label" for="gridRadios2">
          Second radio
        </label>
      </div>
      <div class="bs-form-check bs-disabled">
        <input class="bs-form-check-input" type="radio" name="gridRadios" id="gridRadios3" value="option3" disabled>
        <label class="bs-form-check-label" for="gridRadios3">
          Third disabled radio
        </label>
      </div>
    </div>
  </fieldset>
  <div class="bs-row bs-mb-3">
    <div class="bs-col-sm-10 bs-offset-sm-2">
      <div class="bs-form-check">
        <input class="bs-form-check-input" type="checkbox" id="gridCheck1">
        <label class="bs-form-check-label" for="gridCheck1">
          Example checkbox
        </label>
      </div>
    </div>
  </div>
  <button type="submit" class="bs-btn bs-btn-primary">Sign in</button>
</form>
{{< /example >}}

### Horizontal form label sizing

Be sure to use `.col-form-label-sm` or `.col-form-label-lg` to your `<label>`s or `<legend>`s to correctly follow the size of `.form-control-lg` and `.form-control-sm`.

{{< example >}}
<div class="bs-row bs-mb-3">
  <label for="colFormLabelSm" class="bs-col-sm-2 bs-col-form-label bs-col-form-label-sm">Email</label>
  <div class="bs-col-sm-10">
    <input type="email" class="bs-form-control bs-form-control-sm" id="colFormLabelSm" placeholder="col-form-label-sm">
  </div>
</div>
<div class="bs-row bs-mb-3">
  <label for="colFormLabel" class="bs-col-sm-2 bs-col-form-label">Email</label>
  <div class="bs-col-sm-10">
    <input type="email" class="bs-form-control" id="colFormLabel" placeholder="col-form-label">
  </div>
</div>
<div class="bs-row">
  <label for="colFormLabelLg" class="bs-col-sm-2 bs-col-form-label bs-col-form-label-lg">Email</label>
  <div class="bs-col-sm-10">
    <input type="email" class="bs-form-control bs-form-control-lg" id="colFormLabelLg" placeholder="col-form-label-lg">
  </div>
</div>
{{< /example >}}

## Column sizing

As shown in the previous examples, our grid system allows you to place any number of `.col`s within a `.row`. They'll split the available width equally between them. You may also pick a subset of your columns to take up more or less space, while the remaining `.col`s equally split the rest, with specific column classes like `.col-sm-7`.

{{< example >}}
<div class="bs-row bs-g-3">
  <div class="bs-col-sm-7">
    <input type="text" class="bs-form-control" placeholder="City" aria-label="City">
  </div>
  <div class="bs-col-sm">
    <input type="text" class="bs-form-control" placeholder="State" aria-label="State">
  </div>
  <div class="bs-col-sm">
    <input type="text" class="bs-form-control" placeholder="Zip" aria-label="Zip">
  </div>
</div>
{{< /example >}}

## Auto-sizing

The example below uses a flexbox utility to vertically center the contents and changes `.col` to `.col-auto` so that your columns only take up as much space as needed. Put another way, the column sizes itself based on the contents.

{{< example >}}
<form class="bs-row bs-gy-2 bs-gx-3 bs-align-items-center">
  <div class="bs-col-auto">
    <label class="bs-visually-hidden" for="autoSizingInput">Name</label>
    <input type="text" class="bs-form-control" id="autoSizingInput" placeholder="Jane Doe">
  </div>
  <div class="bs-col-auto">
    <label class="bs-visually-hidden" for="autoSizingInputGroup">Username</label>
    <div class="bs-input-group">
      <div class="bs-input-group-text">@</div>
      <input type="text" class="bs-form-control" id="autoSizingInputGroup" placeholder="Username">
    </div>
  </div>
  <div class="bs-col-auto">
    <label class="bs-visually-hidden" for="autoSizingSelect">Preference</label>
    <select class="bs-form-select" id="autoSizingSelect">
      <option selected>Choose...</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>
  </div>
  <div class="bs-col-auto">
    <div class="bs-form-check">
      <input class="bs-form-check-input" type="checkbox" id="autoSizingCheck">
      <label class="bs-form-check-label" for="autoSizingCheck">
        Remember me
      </label>
    </div>
  </div>
  <div class="bs-col-auto">
    <button type="submit" class="bs-btn bs-btn-primary">Submit</button>
  </div>
</form>
{{< /example >}}

You can then remix that once again with size-specific column classes.

{{< example >}}
<form class="bs-row bs-gx-3 bs-gy-2 bs-align-items-center">
  <div class="bs-col-sm-3">
    <label class="bs-visually-hidden" for="specificSizeInputName">Name</label>
    <input type="text" class="bs-form-control" id="specificSizeInputName" placeholder="Jane Doe">
  </div>
  <div class="bs-col-sm-3">
    <label class="bs-visually-hidden" for="specificSizeInputGroupUsername">Username</label>
    <div class="bs-input-group">
      <div class="bs-input-group-text">@</div>
      <input type="text" class="bs-form-control" id="specificSizeInputGroupUsername" placeholder="Username">
    </div>
  </div>
  <div class="bs-col-sm-3">
    <label class="bs-visually-hidden" for="specificSizeSelect">Preference</label>
    <select class="bs-form-select" id="specificSizeSelect">
      <option selected>Choose...</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>
  </div>
  <div class="bs-col-auto">
    <div class="bs-form-check">
      <input class="bs-form-check-input" type="checkbox" id="autoSizingCheck2">
      <label class="bs-form-check-label" for="autoSizingCheck2">
        Remember me
      </label>
    </div>
  </div>
  <div class="bs-col-auto">
    <button type="submit" class="bs-btn btn-primary">Submit</button>
  </div>
</form>
{{< /example >}}

## Inline forms

Use the `.row-cols-*` classes to create responsive horizontal layouts. By adding [gutter modifier classes]({{< docsref "/layout/gutters" >}}), we'll have gutters in horizontal and vertical directions. On narrow mobile viewports, the `.col-12` helps stack the form controls and more. The `.align-items-center` aligns the form elements to the middle, making the `.form-checkbox` align properly.

{{< example >}}
<form class="bs-row bs-row-cols-lg-auto bs-g-3 bs-align-items-center">
  <div class="bs-col-12">
    <label class="bs-visually-hidden" for="inlineFormInputGroupUsername">Username</label>
    <div class="bs-input-group">
      <div class="bs-input-group-text">@</div>
      <input type="text" class="bs-form-control" id="inlineFormInputGroupUsername" placeholder="Username">
    </div>
  </div>

  <div class="bs-col-12">
    <label class="bs-visually-hidden" for="inlineFormSelectPref">Preference</label>
    <select class="bs-form-select" id="inlineFormSelectPref">
      <option selected>Choose...</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>
  </div>

  <div class="bs-col-12">
    <div class="bs-form-check">
      <input class="bs-form-check-input" type="checkbox" id="inlineFormCheck">
      <label class="bs-form-check-label" for="inlineFormCheck">
        Remember me
      </label>
    </div>
  </div>

  <div class="bs-col-12">
    <button type="submit" class="bs-btn bs-btn-primary">Submit</button>
  </div>
</form>
{{< /example >}}
