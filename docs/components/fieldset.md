---
sidebar_label: "Fieldset"
---

# Fieldset

A flexible fieldset component for grouping form elements with support for different sizes, layouts, and states following BEM methodology.

## Base Usage

The base `.fieldset` component includes a `__legend`, `__content`, and optional `__description`.

<div className="component-preview component-preview--column">
  <fieldset className="fieldset">
    <legend className="fieldset__legend">Personal Information</legend>
    <div className="fieldset__content">
      <div className="input">
        <label className="input__label">Full Name</label>
        <input className="input__field" type="text" placeholder="John Doe" />
      </div>
      <div className="input">
        <label className="input__label">Email</label>
        <input className="input__field" type="email" placeholder="john@example.com" />
      </div>
    </div>
  </fieldset>
</div>

```html
<fieldset class="fieldset">
  <legend class="fieldset__legend">Personal Information</legend>
  <div class="fieldset__content">
    <!-- Form elements go here -->
  </div>
</fieldset>
```

## Variants

### Sizes

Control padding and font sizes using `.fieldset--sm` or `.fieldset--lg`.

<div className="component-preview component-preview--column">
  <fieldset className="fieldset fieldset--sm">
    <legend className="fieldset__legend">Small Fieldset</legend>
    <div className="fieldset__content">
      <div className="input input--sm">
        <input className="input__field" type="text" placeholder="Content..." />
      </div>
    </div>
  </fieldset>

  <fieldset className="fieldset fieldset--lg">
    <legend className="fieldset__legend">Large Fieldset</legend>
    <div className="fieldset__content">
      <div className="input input--lg">
        <input className="input__field" type="text" placeholder="Content..." />
      </div>
    </div>
  </fieldset>
</div>

```html
<!-- Small -->
<fieldset class="fieldset fieldset--sm">...</fieldset>

<!-- Large -->
<fieldset class="fieldset fieldset--lg">...</fieldset>
```

### Layouts

#### Inline

Use `.fieldset--inline` to arrange content horizontally.

<div className="component-preview component-preview--column">
  <fieldset className="fieldset fieldset--inline">
    <legend className="fieldset__legend">Preferences</legend>
    <div className="fieldset__content">
      <label className="checkbox">
        <input type="checkbox" className="checkbox__input" />
        <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
        <span className="checkbox__label">Option 1</span>
      </label>
      <label className="checkbox">
        <input type="checkbox" className="checkbox__input" />
        <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
        <span className="checkbox__label">Option 2</span>
      </label>
    </div>
  </fieldset>
</div>

```html
<fieldset class="fieldset fieldset--inline">
  <!-- Content flows horizontally -->
</fieldset>
```

#### Borderless

Use `.fieldset--borderless` to remove the border and padding, useful for semantic grouping without visual boxing.

<div className="component-preview component-preview--column">
  <fieldset className="fieldset fieldset--borderless">
    <legend className="fieldset__legend">Borderless Group</legend>
    <div className="fieldset__content">
       <div className="input">
        <input className="input__field" type="text" placeholder="Input 1" />
      </div>
    </div>
  </fieldset>
</div>

```html
<fieldset class="fieldset fieldset--borderless">
  <!-- ... -->
</fieldset>
```

## States

### Error State

Use `.fieldset--error` to indicate validation issues at the group level. A `__error` element can be used to display a message.

<div className="component-preview component-preview--column">
  <fieldset className="fieldset fieldset--error">
    <legend className="fieldset__legend">Account Details</legend>
    <p className="fieldset__description">Please fill in your details.</p>
    <div className="fieldset__content">
      <div className="input">
        <input className="input__field" type="text" />
      </div>
    </div>
    <div className="fieldset__error">Please correct the errors above.</div>
  </fieldset>
</div>

```html
<fieldset class="fieldset fieldset--error">
  <legend class="fieldset__legend">Account Details</legend>
  <p class="fieldset__description">Please fill in your details.</p>
  <div class="fieldset__content">
    <!-- ... -->
  </div>
  <div class="fieldset__error">Please correct the errors above.</div>
</fieldset>
```

### Disabled State

Add the `disabled` attribute to the fieldset to disable all interactive elements within it and apply visual styling.

<div className="component-preview component-preview--column">
  <fieldset className="fieldset" disabled>
    <legend className="fieldset__legend">Disabled Group</legend>
    <p className="fieldset__description">This section is not editable.</p>
    <div className="fieldset__content">
      <div className="input">
        <label className="input__label">Name</label>
        <input className="input__field" type="text" placeholder="Cannot type..." />
      </div>
    </div>
  </fieldset>
</div>

```html
<fieldset class="fieldset" disabled>
  <!-- All children inputs/buttons automatically disabled -->
</fieldset>
```
