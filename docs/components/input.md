---
sidebar_position: 3
sidebar_label: "Input"
---

# Input

A flexible input component with support for different sizes, states, icons, and validation messages following BEM methodology.

## Base Usage

The base `.input` component consists of a container with an `__field` element. Labels and helper text can be added as needed.

<div className="component-preview component-preview--center">
  <div className="input">
    <label className="input__label" htmlFor="base-input">Label</label>
    <input className="input__field" type="text" id="base-input" placeholder="Type here..." />
  </div>
</div>

```html
<div class="input">
  <label class="input__label" for="base-input">Label</label>
  <input
    class="input__field"
    type="text"
    id="base-input"
    placeholder="Type here..."
  />
</div>
```

## Sizes

Control the padding and font size using size modifiers on the `.input` block.

<div className="component-preview component-preview--column">
  <div className="input input--xs">
    <label className="input__label">Extra Small</label>
    <input className="input__field" type="text" placeholder="xs input" />
  </div>
  <div className="input input--sm">
    <label className="input__label">Small</label>
    <input className="input__field" type="text" placeholder="sm input" />
  </div>
  <div className="input">
    <label className="input__label">Default</label>
    <input className="input__field" type="text" placeholder="default input" />
  </div>
  <div className="input input--lg">
    <label className="input__label">Large</label>
    <input className="input__field" type="text" placeholder="lg input" />
  </div>
  <div className="input input--xl">
    <label className="input__label">Extra Large</label>
    <input className="input__field" type="text" placeholder="xl input" />
  </div>
    <div className="input input--xxl">
    <label className="input__label">2X Large</label>
    <input className="input__field" type="text" placeholder="xxl input" />
  </div>
</div>

```html
<!-- Extra Small -->
<div class="input input--xs">
  <input class="input__field" type="text" placeholder="xs input" />
</div>

<!-- Small -->
<div class="input input--sm">...</div>

<!-- Default -->
<div class="input">...</div>

<!-- Large -->
<div class="input input--lg">...</div>

<!-- Extra Large -->
<div class="input input--xl">...</div>

<!-- 2X Large -->
<div class="input input--xxl">...</div>
```

## Icons

Use the `.input--icon-left` or `.input--icon-right` modifiers to reserve space for icons. Wrap the field and icon in an `input__wrapper` for positioning.

<div className="component-preview component-preview--column">
    <div className="input input--icon-left">
        <label className="input__label">Left Icon</label>
        <div className="input__wrapper">
            <span className="input__icon input__icon--left">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line></svg>
            </span>
            <input className="input__field" type="text" placeholder="Search..." />
        </div>
    </div>
    
    <div className="input input--icon-right">
        <label className="input__label">Right Icon</label>
        <div className="input__wrapper">
             <input className="input__field" type="text" placeholder="Enter amount" />
             <span className="input__icon input__icon--right">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="12" y1="1" x2="12" y2="23"></line><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path></svg>
            </span>
        </div>
    </div>
</div>

```html
<!-- Left Icon -->
<div class="input input--icon-left">
  <label class="input__label">Left Icon</label>
  <div class="input__wrapper">
    <span class="input__icon input__icon--left">
      <!-- Icon SVG -->
    </span>
    <input class="input__field" type="text" placeholder="Search..." />
  </div>
</div>

<!-- Right Icon -->
<div class="input input--icon-right">
  <label class="input__label">Right Icon</label>
  <div class="input__wrapper">
    <input class="input__field" type="text" placeholder="Enter amount" />
    <span class="input__icon input__icon--right">
      <!-- Icon SVG -->
    </span>
  </div>
</div>
```

## Validation States

Provide visual feedback using validation state modifiers.

### Error State

Use `.input--error` to indicate invalid input. The border, label, and any accompanying error message will use the error color.

<div className="component-preview component-preview--center">
  <div className="input input--error">
    <label className="input__label">Email</label>
    <input className="input__field" type="email" defaultValue="invalid-email" />
     <div className="input__info">
        <span className="input__error">Please enter a valid email address.</span>
    </div>
  </div>
</div>

```html
<div class="input input--error">
  <label class="input__label">Email</label>
  <input class="input__field" type="email" value="invalid-email" />
  <div class="input__info">
    <span class="input__error">Please enter a valid email address.</span>
  </div>
</div>
```

### Success State

Use `.input--success` to indicate valid input.

<div className="component-preview component-preview--center">
  <div className="input input--success">
    <label className="input__label">Username</label>
    <input className="input__field" type="text" defaultValue="validuser123" />
    <div className="input__info">
        <span className="input__success">Username is available!</span>
    </div>
  </div>
</div>

```html
<div class="input input--success">
  <label class="input__label">Username</label>
  <input class="input__field" type="text" value="validuser123" />
  <div class="input__info">
    <span class="input__success">Username is available!</span>
  </div>
</div>
```

## Helper Text

Add informational text below the input using `.input__helper` within an `.input__info` container.

<div className="component-preview component-preview--center">
  <div className="input">
    <label className="input__label">Password</label>
    <input className="input__field" type="password" />
    <div className="input__info">
        <span className="input__helper">Must be at least 8 characters long.</span>
    </div>
  </div>
</div>

```html
<div class="input">
  <label class="input__label">Password</label>
  <input class="input__field" type="password" />
  <div class="input__info">
    <span class="input__helper">Must be at least 8 characters long.</span>
  </div>
</div>
```

## Character Counter

Display a character counter using `.input__counter`. It supports `input__counter--warning` and `input__counter--danger` modifiers.

<div className="component-preview component-preview--column">
  <div className="input">
    <label className="input__label">Bio</label>
    <input className="input__field" type="text" />
    <div className="input__info">
        <span className="input__helper">Brief description</span>
        <span className="input__counter">0/100</span>
    </div>
  </div>
   <div className="input">
    <label className="input__label">Title (Warning)</label>
    <input className="input__field" type="text" defaultValue="Almost too long..." />
    <div className="input__info">
        <span className="input__counter input__counter--warning">90/100</span>
    </div>
  </div>
     <div className="input input--error">
    <label className="input__label">Title (Danger)</label>
    <input className="input__field" type="text" defaultValue="Way too long..." />
    <div className="input__info">
        <span className="input__error">Limit exceeded</span>
        <span className="input__counter input__counter--danger">105/100</span>
    </div>
  </div>
</div>

```html
<div class="input">
  <!-- ... -->
  <div class="input__info">
    <span class="input__helper">Brief description</span>
    <span class="input__counter">0/100</span>
  </div>
</div>
```

## Readonly and Disabled

### Readonly

Use `.input--readonly` for fields that are readable but not editable.

<div className="component-preview component-preview--center">
  <div className="input input--readonly">
    <label className="input__label">API Key</label>
    <input className="input__field" type="text" value="xhQ-29s-..." readOnly />
  </div>
</div>

```html
<div class="input input--readonly">
  <label class="input__label">API Key</label>
  <input class="input__field" type="text" value="xhQ-29s-..." readonly />
</div>
```

### Disabled

Use the `disabled` attribute on the input field.

<div className="component-preview component-preview--center">
  <div className="input">
    <label className="input__label">Disabled Input</label>
    <input className="input__field" type="text" disabled placeholder="Cannot type here" />
  </div>
</div>

```html
<div class="input">
  <label class="input__label">Disabled Input</label>
  <input
    class="input__field"
    type="text"
    disabled
    placeholder="Cannot type here"
  />
</div>
```
