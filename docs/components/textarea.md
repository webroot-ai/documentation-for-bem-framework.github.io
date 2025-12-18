---
sidebar_position: 2
sidebar_label: "Textarea"
---

# Textarea

A multi-line text input component that supports various sizes, validation states, and floating label interactions.

## Base Usage

The base `.textarea` class provides a standard multi-line input field.

<div className="component-preview component-preview--center">
  <textarea className="textarea" placeholder="Enter your comments..." rows="5" cols="30"></textarea>
</div>

```html
<textarea
  class="textarea"
  placeholder="Enter your comments..."
  rows="5"
  cols="30"
></textarea>
```

## Validation States

Provide visual feedback for form validation using success and error states.

### Error State

Add `.textarea--error` to indicate an invalid input.

<div className="component-preview component-preview--center">
  <textarea className="textarea textarea--error" placeholder="Invalid input..." rows="5" cols="30"></textarea>
</div>

```html
<textarea
  class="textarea textarea--error"
  placeholder="Invalid input..."
></textarea>
```

### Success State

Add `.textarea--success` to indicate a valid input.

<div className="component-preview component-preview--center">
  <textarea className="textarea textarea--success" placeholder="Valid input..." rows="5" cols="30"></textarea>
</div>

```html
<textarea
  class="textarea textarea--success"
  placeholder="Valid input..."
></textarea>
```

## Size Variants

Control the font size and padding using size modifiers.

<div className="component-preview component-preview--center">
  <textarea className="textarea textarea--xs" placeholder="Extra Small" rows="2"></textarea>
  <textarea className="textarea textarea--sm" placeholder="Small" rows="2"></textarea>
  <textarea className="textarea" placeholder="Default" rows="2"></textarea>
  <textarea className="textarea textarea--lg" placeholder="Large" rows="2"></textarea>
  <textarea className="textarea textarea--xl" placeholder="Extra Large" rows="2"></textarea>
</div>

| Size        | Class           | Description                |
| ----------- | --------------- | -------------------------- |
| Extra Small | `.textarea--xs` | Compact padding & text     |
| Small       | `.textarea--sm` | Slightly smaller than base |
| Default     | `.textarea`     | Standard size              |
| Large       | `.textarea--lg` | Larger padding & text      |
| Extra Large | `.textarea--xl` | Maximum padding & text     |

```html
<textarea class="textarea textarea--xs" placeholder="Extra Small"></textarea>
<textarea class="textarea textarea--sm" placeholder="Small"></textarea>
<textarea class="textarea" placeholder="Default"></textarea>
<textarea class="textarea textarea--lg" placeholder="Large"></textarea>
<textarea class="textarea textarea--xl" placeholder="Extra Large"></textarea>
```

## Layout Modifiers

### Fluid Width

Use `.textarea--fluid` to make the textarea take up 100% of its container's width.

<div className="component-preview component-preview--column">
  <textarea className="textarea textarea--fluid" placeholder="Full width textarea..."></textarea>
</div>

```html
<textarea
  class="textarea textarea--fluid"
  placeholder="Full width textarea..."
></textarea>
```

## Floating Labels

The framework supports three types of floating label interactions. These require a specific HTML structure:

1. Wrap the textarea and label in a `.textarea-wrapper` container.
2. Place the `<label>` **after** the `<textarea>` in the DOM.
3. Add the `.textarea__label` class to the label.
4. Add the `placeholder=" "` attribute (single space) to the textarea to trigger the CSS state detection.

### Over Label

The label floats from inside the textarea to above it.

<div className="component-preview component-preview--center">
  <div className="textarea-wrapper">
    <textarea className="textarea over-label" placeholder=" " id="over-label-ex"></textarea>
    <label className="textarea__label" htmlFor="over-label-ex">Over Label</label>
  </div>
</div>

```html
<div class="textarea-wrapper">
  <textarea class="textarea over-label" placeholder=" " id="comment"></textarea>
  <label class="textarea__label" for="comment">Type your comment</label>
</div>
```

### In Label

The label moves to the top-inner corner of the textarea.

<div className="component-preview component-preview--center">
  <div className="textarea-wrapper">
    <textarea className="textarea in-label" placeholder=" " id="in-label-ex"></textarea>
    <label className="textarea__label" htmlFor="in-label-ex">In Label</label>
  </div>
</div>

```html
<div class="textarea-wrapper">
  <textarea class="textarea in-label" placeholder=" " id="comment"></textarea>
  <label class="textarea__label" for="comment">Type your comment</label>
</div>
```

### On Label

The label creates a "cut-out" effect on the top border.

<div className="component-preview component-preview--center">
  <div className="textarea-wrapper">
    <textarea className="textarea on-label" placeholder=" " id="on-label-ex"></textarea>
    <label className="textarea__label" htmlFor="on-label-ex">On Label</label>
  </div>
</div>

```html
<div class="textarea-wrapper">
  <textarea class="textarea on-label" placeholder=" " id="comment"></textarea>
  <label class="textarea__label" for="comment">Type your comment</label>
</div>
```

## Resize

The textarea can be resized using the `resize` modifier. This default state lets you resize the textarea both horizontally and vertically. By default, the textarea is not resizable.

<div className="component-preview component-preview--center">
  <textarea className="textarea textarea--resize" placeholder="Enter your comments..." rows="5" cols="30"></textarea>
</div>

```html
<textarea
  class="textarea textarea--resize"
  placeholder="Enter your comments..."
  rows="5"
  cols="30"
></textarea>
```

### Resize X

The textarea can be resized horizontally using the `resize-x` modifier.

<div className="component-preview component-preview--center">
  <textarea className="textarea textarea--resize-x" placeholder="Enter your comments..." rows="5" cols="30"></textarea>
</div>

```html
<textarea
  class="textarea textarea--resize-x"
  placeholder="Enter your comments..."
  rows="5"
  cols="30"
></textarea>
```

### Resize Y

The textarea can be resized vertically using the `resize-y` modifier.

<div className="component-preview component-preview--center">
  <textarea className="textarea textarea--resize-y" placeholder="Enter your comments..." rows="5" cols="30"></textarea>
</div>

```html
<textarea
  class="textarea textarea--resize-y"
  placeholder="Enter your comments..."
  rows="5"
  cols="30"
></textarea>
```

## Accessibility

- **Labels**: Always ensure every textarea has an associated label. For floating labels, use the `for` attribute on the label and `id` on the textarea.
- **Focus**: The component uses `.focus-visible` to show a primary colored border when focused via keyboard.
- **Disabled**: Disabled textareas have reduced opacity and `not-allowed` cursor.

## CSS Custom Properties

| Property                  | Description          |
| ------------------------- | -------------------- |
| `--text-base`             | Font size reference  |
| `--font-medium`           | Font weight          |
| `--color-secondary`       | Default border color |
| `--color-secondary-hover` | Hover border color   |
| `--color-primary`         | Focus border color   |
| `--color-error`           | Error state color    |
| `--color-success`         | Success state color  |
