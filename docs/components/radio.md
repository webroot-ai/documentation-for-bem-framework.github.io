---
sidebar_position: 4
sidebar_label: "Radio"
---

# Radio

A customizable radio button component with support for sizes, states, and group layouts.

## Basic Usage

The radio component uses a hidden native input and custom styled elements (`__box` and `__icon`) to create the visual appearance.

<div className="component-preview component-preview--center">
  <div className="radio-group radio-group--col">
    <label className="radio">
      <input type="radio" name="preview-basic" value="1" defaultChecked />
      <span className="radio__box">
        <span className="radio__icon"></span>
      </span>
      <span className="radio__label">Option 1</span>
    </label>
  </div>
</div>

```html
<label class="radio">
  <input type="radio" name="group1" value="option1" checked />
  <span class="radio__box">
    <span class="radio__icon"></span>
  </span>
  <span class="radio__label">Option 1</span>
</label>
```

## Sizes

Use size modifiers to adjust the dimensions of the radio button and label text.

<div className="component-preview component-preview--column">
  
  <label className="radio radio--sm">
    <input type="radio" name="preview-size" value="sm" defaultChecked />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Small Radio (.radio--sm)</span>
  </label>

  <label className="radio">
    <input type="radio" name="preview-size" value="md" />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Default Radio</span>
  </label>

  <label className="radio radio--lg">
    <input type="radio" name="preview-size" value="lg" />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Large Radio (.radio--lg)</span>
  </label>

</div>

```html
<!-- Small -->
<label class="radio radio--sm" checked>...</label>

<!-- Default -->
<label class="radio">...</label>

<!-- Large -->
<label class="radio radio--lg">...</label>
```

## States

### Error

Use `.radio--error` to indicate an invalid selection.

<div className="component-preview component-preview--center">
  <label className="radio radio--error">
    <input type="radio" name="preview-error" defaultChecked />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Invalid Selection</span>
  </label>
   <label className="radio radio--error">
    <input type="radio" name="preview-error" />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Wrong Selection</span>
  </label>
</div>

```html
<label class="radio radio--error">
  <input type="radio" name="group" checked />
  <span class="radio__box"><span class="radio__icon"></span></span>
  <span class="radio__label">Invalid Selection</span>
</label>

<label class="radio radio--error">
  <input type="radio" name="group" />
  <span class="radio__box"><span class="radio__icon"></span></span>
  <span class="radio__label">Wrong Selection</span>
</label>
```

### Disabled

Use `.radio--disabled` or the `disabled` attribute on the input.

<div className="component-preview component-preview--column">
  <label className="radio radio--disabled">
    <input type="radio" name="preview-disabled" disabled />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Disabled Unchecked</span>
  </label>

   <label className="radio radio--disabled">
    <input type="radio" name="preview-disabled" defaultChecked disabled />
    <span className="radio__box"><span className="radio__icon"></span></span>
    <span className="radio__label">Disabled Checked</span>
  </label>
</div>

```html
<label class="radio radio--disabled">
  <input type="radio" disabled />
  <!-- ... -->
</label>
```

## Radio Groups

Wrap multiple radio buttons in `.radio-group` to handle layout.

### Group with Label

Add a `.radio-group__label` inside the container to title the group.

<div className="component-preview">
  <div className="radio-group radio-group--row">
    <div className="radio-group__label">Choose Your Topping:</div>
    <label className="radio">
      <input type="radio" name="topping" defaultChecked/> 
      <span className="radio__box"><span className="radio__icon"></span></span>
      <span className="radio__label">Pepperoni</span>
    </label>
    <label className="radio">
      <input type="radio" name="topping" /> 
      <span className="radio__box"><span className="radio__icon"></span></span>
      <span className="radio__label">Mushrooms</span>
    </label>
  </div>
</div>

```html
<div class="radio-group radio-group--row">
  <div class="radio-group__label">Choose Your Topping:</div>
  <!-- ... radios ... -->
</div>
```

### Column Layout

Use `.radio-group--col` to stack items vertically.

<div className="component-preview">
  <div className="radio-group radio-group--col">
    <div className="radio-group__label">Select Meal Time:</div>
    <label className="radio">
        <input type="radio" name="group-col" defaultChecked/> 
        <span className="radio__box"><span className="radio__icon"></span></span>
        <span className="radio__label">Breakfast</span>
    </label>
    <label className="radio">
        <input type="radio" name="group-col" /> 
        <span className="radio__box"><span className="radio__icon"></span></span>
        <span className="radio__label">Lunch</span>
    </label>
    <label className="radio">
        <input type="radio" name="group-col" /> 
        <span className="radio__box"><span className="radio__icon"></span></span>
        <span className="radio__label">Dinner</span>
    </label>
  </div>
</div>

```html
<div class="radio-group radio-group--col">
  <span class="radio-group__label">Select Meal Time:</span>
  <label class="radio">
    <input type="radio" name="meal" checked />
    <span class="radio__box"><span class="radio__icon"></span></span>
    <span class="radio__label">Breakfast</span>
  </label>
  <label class="radio">
    <input type="radio" name="meal" />
    <span class="radio__box"><span class="radio__icon"></span></span>
    <span class="radio__label">Lunch</span>
  </label>
</div>
```

### Row Layout

Use `.radio-group--row` to arrange items horizontally.

<div className="component-preview">
  <div className="radio-group radio-group--row">
    <label className="radio">
      <input type="radio" name="group-row" defaultChecked/> 
      <span className="radio__box"><span className="radio__icon"></span></span>
      <span className="radio__label">Option A</span>
    </label>
    <label className="radio">
      <input type="radio" name="group-row" /> 
      <span className="radio__box"><span className="radio__icon"></span></span>
      <span className="radio__label">Option B</span>
    </label>
      <label className="radio">
      <input type="radio" name="group-row" /> 
      <span className="radio__box"><span className="radio__icon"></span></span>
      <span className="radio__label">Option C</span>
    </label>
  </div>
</div>

```html
<div class="radio-group radio-group--row">
  <!-- radio buttons -->
</div>
```
