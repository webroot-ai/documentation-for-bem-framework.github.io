---
sidebar_label: "Select"
---

# Select

A flexible select (dropdown) component with support for different sizes, states, and validation messages following BEM methodology.

## Base Usage

The base `.select` component consists of a `__label`, and a `__wrapper` containing the `__field` (the `<select>` element) and a custom `__arrow` icon.

<div className="component-preview component-preview--center">
  <div className="select">
    <label className="select__label" htmlFor="base-select">Choose an option</label>
    <div className="select__wrapper">
      <select className="select__field" id="base-select">
        <option>Option 1</option>
        <option>Option 2</option>
        <option>Option 3</option>
      </select>
      <span className="select__arrow"></span>
    </div>
  </div>
</div>

```html
<div class="select">
  <label class="select__label" for="base-select">Choose an option</label>
  <div class="select__wrapper">
    <select class="select__field" id="base-select">
      <option>Option 1</option>
      <option>Option 2</option>
      <option>Option 3</option>
    </select>
    <span class="select__arrow"></span>
  </div>
</div>
```

## Variants

### Sizes

Control the size using modifiers: `.select--xs`, `.select--sm`, `.select--lg`, `.select--xl`, `.select--xxl`.

<div className="component-preview component-preview--column">
  <div className="select select--xs">
    <div className="select__wrapper">
        <select className="select__field"><option>Extra Small</option></select>
        <span className="select__arrow"></span>
    </div>
  </div>
    <div className="select select--sm">
    <div className="select__wrapper">
        <select className="select__field"><option>Small</option></select>
        <span className="select__arrow"></span>
    </div>
  </div>
  <div className="select">
    <div className="select__wrapper">
        <select className="select__field"><option>Default</option></select>
        <span className="select__arrow"></span>
    </div>
  </div>
  <div className="select select--lg">
    <div className="select__wrapper">
        <select className="select__field"><option>Large</option></select>
        <span className="select__arrow"></span>
    </div>
  </div>
  <div className="select select--xl">
    <div className="select__wrapper">
        <select className="select__field"><option>Extra Large</option></select>
        <span className="select__arrow"></span>
    </div>
  </div>
</div>

```html
<div class="select select--xs">...</div>
<div class="select select--sm">...</div>
<div class="select">...</div>
<div class="select select--lg">...</div>
<div class="select select--xl">...</div>
```

### Multiple Select

Use `.select--multiple` for multi-select fields. Note that the custom arrow is hidden in this mode.

<div className="component-preview component-preview--center">
  <div className="select select--multiple">
    <label className="select__label">Choose multiple</label>
    <div className="select__wrapper">
      <select className="select__field" multiple>
        <option>Option 1</option>
        <option>Option 2</option>
        <option>Option 3</option>
        <option>Option 4</option>
      </select>
      <span className="select__arrow"></span>
    </div>
  </div>
</div>

```html
<div class="select select--multiple">
  <label class="select__label">Choose multiple</label>
  <div class="select__wrapper">
    <select class="select__field" multiple>
      <!-- options -->
    </select>
    <span class="select__arrow"></span>
  </div>
</div>
```

## States

### Validation

Use `.select--error` or `.select--success` states. Message elements `__error` or `__success` can be placed inside `__info`.

<div className="component-preview component-preview--column">
  <div className="select select--error">
    <label className="select__label">Error State</label>
    <div className="select__wrapper">
      <select className="select__field">
        <option>Invalid Selection</option>
      </select>
      <span className="select__arrow"></span>
    </div>
    <div className="select__info">
      <span className="select__error">Please make a valid selection.</span>
    </div>
  </div>

  <div className="select select--success">
    <label className="select__label">Success State</label>
    <div className="select__wrapper">
      <select className="select__field">
        <option>Valid Selection</option>
      </select>
      <span className="select__arrow"></span>
    </div>
    <div className="select__info">
      <span className="select__success">Selection confirmed.</span>
    </div>
  </div>
</div>

```html
<!-- Error -->
<div class="select select--error">
  <!-- ... -->
  <div class="select__info">
    <span class="select__error">message</span>
  </div>
</div>

<!-- Success -->
<div class="select select--success">
  <!-- ... -->
  <div class="select__info">
    <span class="select__success">message</span>
  </div>
</div>
```

### Disabled

Use `.select--disabled` or the `disabled` attribute on the select element.

<div className="component-preview component-preview--center">
  <div className="select select--disabled">
    <label className="select__label">Disabled</label>
    <div className="select__wrapper">
      <select className="select__field" disabled>
        <option>Unavailable</option>
      </select>
      <span className="select__arrow"></span>
    </div>
  </div>
</div>

```html
<div class="select select--disabled">
  <label class="select__label">Disabled</label>
  <div class="select__wrapper">
    <select class="select__field" disabled>
      <option>Unavailable</option>
    </select>
    <span class="select__arrow"></span>
  </div>
</div>
```
