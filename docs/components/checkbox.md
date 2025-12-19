---
sidebar_label: "Checkbox"
---

# Checkbox

A flexible checkbox component with support for different sizes, states, and descriptions following BEM methodology.

## Base Usage

The base `.checkbox` component consists of a label containing a hidden input `__input`, a custom visual `__box`, a checkmark `__checkmark`, and a `__label` text.

<div className="component-preview component-preview--center">
  <label className="checkbox">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box">
      <span className="checkbox__checkmark"></span>
    </span>
    <span className="checkbox__label">Accept terms and conditions</span>
  </label>
</div>

```html
<label class="checkbox">
  <input type="checkbox" class="checkbox__input" />
  <span class="checkbox__box">
    <span class="checkbox__checkmark"></span>
  </span>
  <span class="checkbox__label">Accept terms and conditions</span>
</label>
```

## Variants

### Sizes

Control the size using modifiers: `.checkbox--xs`, `.checkbox--sm`, `.checkbox--lg`, `.checkbox--xl`.

<div className="component-preview component-preview--column">
  <label className="checkbox checkbox--xs">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Extra Small</span>
  </label>
  <label className="checkbox checkbox--sm">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Small</span>
  </label>
  <label className="checkbox">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Default</span>
  </label>
  <label className="checkbox checkbox--lg">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Large</span>
  </label>
  <label className="checkbox checkbox--xl">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Extra Large</span>
  </label>
</div>

```html
<label class="checkbox checkbox--xs">...</label>
<label class="checkbox checkbox--sm">...</label>
<label class="checkbox">...</label>
<label class="checkbox checkbox--lg">...</label>
<label class="checkbox checkbox--xl">...</label>
```

### Layout

Use `.checkbox--label-left` to position the label text to the left of the checkbox.

<div className="component-preview component-preview--center">
  <label className="checkbox checkbox--label-left">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Label on Left</span>
  </label>
</div>

```html
<label class="checkbox checkbox--label-left">
  <!-- ... structure ... -->
</label>
```

## States

### Indeterminate

Use `.checkbox--indeterminate` for partially selected states (e.g., parent checkboxes). This state displays a minus icon instead of a checkmark.

<div className="component-preview component-preview--center">
  <label className="checkbox checkbox--indeterminate">
    <input type="checkbox" className="checkbox__input" defaultChecked />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Indeterminate</span>
  </label>
</div>

```html
<label class="checkbox checkbox--indeterminate">
  <input type="checkbox" class="checkbox__input" checked />
  <span class="checkbox__box">
    <span class="checkbox__checkmark"></span>
  </span>
  <span class="checkbox__label">Indeterminate</span>
</label>
```

### Error

Use `.checkbox--error` to indicate validation errors.

<div className="component-preview component-preview--center">
  <label className="checkbox checkbox--error">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">I agree to the terms</span>
  </label>
</div>

```html
<label class="checkbox checkbox--error">
  <!-- ... -->
</label>
```

### Disabled

Add the `.checkbox--disabled` class and/or the `disabled` attribute to the input.

<div className="component-preview component-preview--center">
  <label className="checkbox checkbox--disabled">
    <input type="checkbox" className="checkbox__input" disabled />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Disabled</span>
  </label>
  <label className="checkbox checkbox--disabled">
    <input type="checkbox" className="checkbox__input" checked disabled />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__label">Disabled Checked</span>
  </label>
</div>

```html
<label class="checkbox checkbox--disabled">
  <input type="checkbox" class="checkbox__input" disabled />
  <!-- ... -->
</label>
```

## With Description

Use `__text-container` to group the label and a `__description` element.

<div className="component-preview component-preview--center">
  <label className="checkbox">
    <input type="checkbox" className="checkbox__input" />
    <span className="checkbox__box"><span className="checkbox__checkmark"></span></span>
    <span className="checkbox__text-container">
      <span className="checkbox__label">Subscribe to newsletter</span>
      <span className="checkbox__description">Receive the latest updates and news directly to your inbox.</span>
    </span>
  </label>
</div>

```html
<label class="checkbox">
  <input type="checkbox" class="checkbox__input" />
  <span class="checkbox__box">
    <span class="checkbox__checkmark"></span>
  </span>
  <span class="checkbox__text-container">
    <span class="checkbox__label">Subscribe to newsletter</span>
    <span class="checkbox__description"
      >Receive the latest updates and news directly to your inbox.</span
    >
  </span>
</label>
```
