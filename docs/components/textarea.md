---
sidebar_position: 4
sidebar_label: "Textarea"
---

# Textarea

A flexible multi-line text input component that supports various sizes, states, character counts, and floating label interactions following BEM methodology.

## Base Usage

The base `.textarea` component consists of a container with a `__field` element. Labels and helper text should be added for accessibility and clarity.

<div className="component-preview component-preview--center">
  <div className="textarea">
    <label className="textarea__label" htmlFor="base-textarea">Description</label>
    <textarea className="textarea__field" id="base-textarea" placeholder="Enter your comments..."></textarea>
  </div>
</div>

```html
<div class="textarea">
  <label class="textarea__label" for="base-textarea">Description</label>
  <textarea
    class="textarea__field"
    id="base-textarea"
    placeholder="Enter your comments..."
  ></textarea>
</div>
```

## Validation States

Provide visual feedback using validation state modifiers on the `.textarea` wrapper.

### Error State

Use `.textarea--error` to indicate invalid input. The border, label, and any accompanying error message will use the error color.

<div className="component-preview component-preview--center">
  <div className="textarea textarea--error">
    <label className="textarea__label">Comment</label>
    <textarea className="textarea__field" placeholder="Enter comment..."></textarea>
     <div className="textarea__info">
        <span className="textarea__error">This field is required.</span>
    </div>
  </div>
</div>

```html
<div class="textarea textarea--error">
  <label class="textarea__label">Comment</label>
  <textarea class="textarea__field" placeholder="Enter comment..."></textarea>
  <div class="textarea__info">
    <span class="textarea__error">This field is required.</span>
  </div>
</div>
```

### Success State

Use `.textarea--success` to indicate valid input.

<div className="component-preview component-preview--center">
  <div className="textarea textarea--success">
    <label className="textarea__label">Feedback</label>
    <textarea className="textarea__field" defaultValue="Great service!"></textarea>
    <div className="textarea__info">
        <span className="textarea__success">Feedback saved!</span>
    </div>
  </div>
</div>

```html
<div class="textarea textarea--success">
  <label class="textarea__label">Feedback</label>
  <textarea class="textarea__field">Great service!</textarea>
  <div class="textarea__info">
    <span class="textarea__success">Feedback saved!</span>
  </div>
</div>
```

## Helper Text & Character Counter

Use the `.textarea__info` container to display helper text and character counters.

### Basic Helper

<div className="component-preview component-preview--center">
  <div className="textarea">
    <label className="textarea__label">Bio</label>
    <textarea className="textarea__field"></textarea>
    <div className="textarea__info">
        <span className="textarea__helper">Tell us a bit about yourself.</span>
    </div>
  </div>
</div>
```html
<div class="textarea">
  <label class="textarea__label">Bio</label>
  <textarea class="textarea__field"></textarea>
  <div class="textarea__info">
    <span class="textarea__helper">Tell us a bit about yourself.</span>
  </div>
</div>
```

### Character Counter

The `__counter` element supports `--warning` and `--danger` states.

### Basic Counter

<div className="component-preview component-preview--center">
  <div className="textarea">
    <label className="textarea__label">Review</label>
    <textarea className="textarea__field"></textarea>
    <div className="textarea__info">
        <span className="textarea__helper">Max 100 chars</span>
        <span className="textarea__counter">0/100</span>
    </div>
  </div>
</div>
```html
<div class="textarea">
  <label class="textarea__label">Review</label>
  <textarea class="textarea__field"></textarea>
  <div class="textarea__info">
    <span class="textarea__helper">Max 100 chars</span>
    <span class="textarea__counter">0/100</span>
  </div>
</div>
```

### Warning Counter

<div className="component-preview component-preview--center">
  <div className="textarea">
    <label className="textarea__label">Review</label>
    <textarea className="textarea__field"></textarea>
    <div className="textarea__info">
        <span className="textarea__helper">Max 100 chars</span>
        <span className="textarea__counter textarea__counter--warning">0/100</span>
    </div>
  </div>
</div>
```html
<div class="textarea">
  <label class="textarea__label">Review</label>
  <textarea class="textarea__field"></textarea>
  <div class="textarea__info">
    <span class="textarea__helper">Max 100 chars</span>
    <span class="textarea__counter textarea__counter--warning">0/100</span>
  </div>
</div>
```

### Error State

<div className="textarea textarea--error">
    <label className="textarea__label">Error State</label>
    <textarea className="textarea__field" defaultValue="Text is way too long for this field so we show an error."></textarea>
    <div className="textarea__info">
        <span className="textarea__error">Limit exceeded</span>
        <span className="textarea__counter textarea__counter--danger">150/100</span>
    </div>
</div>
```html
<div class="textarea textarea--error">
  <label class="textarea__label">Error state</label>
  <textarea class="textarea__field">Text is way too long for this field so we show an error.</textarea>
  <div class="textarea__info">
    <span class="textarea__error">Limit exceeded</span>
    <span class="textarea__counter textarea__counter--danger">150/100</span>
  </div>
</div>
```

## Resize Modifiers

Control how the user can resize the textarea. the

| Modifier                 | Description                     |
| :----------------------- | :------------------------------ |
| `.textarea--resize-both` | Allows resizing both dimensions |
| `.textarea--resize-x`    | Allows horizontal resizing      |
| `.textarea--resize-y`    | Allows vertical resizing        |

<div className="component-preview component-preview--center">
  <div className="textarea textarea--resize-both">
    <label className="textarea__label">Resize vertically and horizontally</label>
    <textarea className="textarea__field"></textarea>
  </div>
  <div className="textarea textarea--resize-x">
    <label className="textarea__label">Resize horizontally</label>
    <textarea className="textarea__field"></textarea>
  </div>
  <div className="textarea textarea--resize-y">
    <label className="textarea__label">Vertical Only</label>
    <textarea className="textarea__field"></textarea>
  </div>
</div>

```html
<div class="textarea textarea--resize-both">
  <textarea class="textarea__field" defaultValue=""></textarea>
</div>
<div class="textarea textarea--resize-x">
  <textarea class="textarea__field" defaultValue=""></textarea>
</div>
<div class="textarea textarea--resize-y">
  <textarea class="textarea__field"></textarea>
</div>
```

## Floating Labels

The framework supports three types of floating label interactions.
**Note:** For floating labels to work, the `<label>` must come **after** the `<textarea>` in the HTML, and the textarea needs a placeholder (can be empty space).

### Over Label

The label floats from inside the textarea to above it.

<div className="component-preview component-preview--center">
  <div className="textarea textarea--over-label">
    <textarea className="textarea__field" placeholder=" " id="over-label-ex"></textarea>
    <label className="textarea__label" htmlFor="over-label-ex">Over Label</label>
  </div>
</div>

```html
<div class="textarea textarea--over-label">
  <textarea class="textarea__field" placeholder=" " id="desc"></textarea>
  <label class="textarea__label" for="desc">Description</label>
</div>
```

### In Label

The label moves to the top-inner corner of the textarea.

<div className="component-preview component-preview--center">
  <div className="textarea textarea--in-label">
    <textarea className="textarea__field" placeholder=" " id="in-label-ex"></textarea>
    <label className="textarea__label" htmlFor="in-label-ex">In Label</label>
  </div>
</div>

### On Label

The label creates a "cut-out" effect on the top border.

<div className="component-preview component-preview--center">
  <div className="textarea textarea--on-label">
    <textarea className="textarea__field" placeholder=" " id="on-label-ex"></textarea>
    <label className="textarea__label" htmlFor="on-label-ex">On Label</label>
  </div>
</div>

```html
<div class="textarea textarea--on-label">
  <textarea class="textarea__field" placeholder=" " id="notes"></textarea>
  <label class="textarea__label" for="notes">Notes</label>
</div>
```

## Readonly & Disabled

<div className="component-preview component-preview--column">
  <div className="textarea textarea--readonly">
    <label className="textarea__label">Readonly</label>
    <textarea className="textarea__field" readOnly defaultValue="Thie text cannot be edited."></textarea>
  </div>
   <div className="textarea">
    <label className="textarea__label">Disabled</label>
    <textarea className="textarea__field" disabled defaultValue="This input is disabled."></textarea>
  </div>
</div>

```html
<div class="textarea textarea--readonly">
  <textarea class="textarea__field" readonly>Value</textarea>
</div>

<div class="textarea">
  <textarea class="textarea__field" disabled>Value</textarea>
</div>
```
