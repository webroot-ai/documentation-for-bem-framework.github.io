---
sidebar_position: 1
sidebar_label: "Button"
---

# Button

A flexible, accessible button component built with BEM methodology. The button supports multiple variants, sizes, shapes, and states.

## Base Usage

The base `.button` class provides a primary styled button with hover, active, focus, and disabled states.

<div className="component-preview component-preview--center">
  <button className="button">Primary Button</button>
</div>

```html
<button class="button">Primary Button</button>
```

## Variants

### Color Variants

<div className="component-preview component-preview--center">
  <button className="button">Primary</button>
  <button className="button button--secondary">Secondary</button>
  <button className="button button--outlined">Outlined</button>
  <button className="button button--ghost">Ghost</button>
  <button className="button button--success">Success</button>
  <button className="button button--warning">Warning</button>
  <button className="button button--danger">Danger</button>
</div>

| Modifier          | Class                       | Description                         |
| ----------------- | --------------------------- | ----------------------------------- |
| Primary (default) | `.button`                   | Default blue primary action button  |
| Secondary         | `.button.button--secondary` | Gray secondary action button        |
| Outlined          | `.button.button--outlined`  | Transparent with border             |
| Ghost             | `.button.button--ghost`     | Minimal, borderless button          |
| Success           | `.button.button--success`   | Green success/confirmation button   |
| Warning           | `.button.button--warning`   | Amber warning button                |
| Danger            | `.button.button--danger`    | Red error/destructive action button |

```html
<button class="button">Primary</button>
<button class="button button--secondary">Secondary</button>
<button class="button button--outlined">Outlined</button>
<button class="button button--ghost">Ghost</button>
<button class="button button--success">Success</button>
<button class="button button--warning">Warning</button>
<button class="button button--danger">Danger</button>
```

### Size Variants

<div className="component-preview component-preview--center">
  <button className="button button--xs">Extra Small</button>
  <button className="button button--sm">Small</button>
  <button className="button">Default</button>
  <button className="button button--lg">Large</button>
  <button className="button button--xl">Extra Large</button>
</div>

| Size        | Class                | Description                   |
| ----------- | -------------------- | ----------------------------- |
| Extra Small | `.button.button--xs` | Compact size for dense UIs    |
| Small       | `.button.button--sm` | Smaller than default          |
| Default     | `.button`            | Standard button size          |
| Large       | `.button.button--lg` | Larger for prominent actions  |
| Extra Large | `.button.button--xl` | Maximum size for hero actions |

```html
<button class="button button--xs">Extra Small</button>
<button class="button button--sm">Small</button>
<button class="button">Default</button>
<button class="button button--lg">Large</button>
<button class="button button--xl">Extra Large</button>
```

### Shape Variants

<div className="component-preview component-preview--center">
  <button className="button button--rounded">Rounded</button>
  <button className="button button--square">■</button>
  <button className="button button--circle">⭐</button>
</div>

<div className="component-preview component-preview--column">
  <button className="button button--block">Full Width (Block)</button>
</div>

| Shape   | Class                     | Description                         |
| ------- | ------------------------- | ----------------------------------- |
| Default | `.button`                 | Standard rounded corners (8px)      |
| Rounded | `.button.button--rounded` | Pill-shaped (fully rounded)         |
| Square  | `.button.button--square`  | Equal width/height for icon buttons |
| Circle  | `.button.button--circle`  | Circular for icon-only buttons      |
| Block   | `.button.button--block`   | Full-width button                   |

```html
<button class="button button--rounded">Rounded</button>
<button class="button button--square">■</button>
<button class="button button--circle">⭐</button>
<button class="button button--block">Full Width</button>
```

## Elements

Buttons can contain child elements using BEM element classes:

### Icon + Text

<div className="component-preview component-preview--center">
  <button className="button">
    <span className="button__icon">🔍</span>
    <span className="button__text">Search</span>
  </button>
  <button className="button button--success">
    <span className="button__icon">✓</span>
    <span className="button__text">Confirm</span>
  </button>
  <button className="button button--danger">
    <span className="button__icon">🗑</span>
    <span className="button__text">Delete</span>
  </button>
</div>

```html
<button class="button">
  <span class="button__icon">🔍</span>
  <span class="button__text">Search</span>
</button>
```

## States

### Loading State

Add `.is-loading` class to show a loading spinner:

<div className="component-preview component-preview--center">
  <button className="button is-loading">Loading...</button>
  <button className="button button--secondary is-loading">Loading...</button>
  <button className="button button--success is-loading">Loading...</button>
</div>

```html
<button class="button is-loading">Loading...</button>
```

The loading state:

- Makes text transparent
- Shows a centered spinner animation
- Disables pointer events

### Active/Selected State

Add `.is-active` class for toggle or selected buttons:

<div className="component-preview component-preview--center">
  <button className="button">Normal</button>
  <button className="button is-active">Active</button>
</div>

```html
<button class="button is-active">Selected</button>
```

### Disabled State

Use the `disabled` attribute or `.is-disabled` class:

<div className="component-preview component-preview--center">
  <button className="button" disabled>Disabled Primary</button>
  <button className="button button--secondary" disabled>Disabled Secondary</button>
  <button className="button button--outlined is-disabled">Disabled Outlined</button>
</div>

```html
<button class="button" disabled>Disabled</button>
<button class="button is-disabled">Also Disabled</button>
```

## Button Groups

Use `.button-group` to group related buttons together.

### Basic Group

<div className="component-preview component-preview--center">
  <div className="button-group">
    <button className="button">One</button>
    <button className="button">Two</button>
    <button className="button">Three</button>
  </div>
</div>

```html
<div class="button-group">
  <button class="button">One</button>
  <button class="button">Two</button>
  <button class="button">Three</button>
</div>
```

### Attached Group

Use `.button-group--attached` for seamlessly connected buttons:

<div className="component-preview component-preview--center">
  <div className="button-group button-group--attached">
    <button className="button">Left</button>
    <button className="button">Center</button>
    <button className="button">Right</button>
  </div>
</div>

```html
<div class="button-group button-group--attached">
  <button class="button">Left</button>
  <button class="button">Center</button>
  <button class="button">Right</button>
</div>
```

### Vertical Group

Use `.button-group--vertical` for stacked buttons:

<div className="component-preview component-preview--center">
  <div className="button-group button-group--vertical">
    <button className="button">Top</button>
    <button className="button">Middle</button>
    <button className="button">Bottom</button>
  </div>
</div>

```html
<div class="button-group button-group--vertical">
  <button class="button">Top</button>
  <button class="button">Middle</button>
  <button class="button">Bottom</button>
</div>
```

### Vertical Attached Group

<div className="component-preview component-preview--center">
  <div className="button-group button-group--vertical button-group--attached">
    <button className="button">Top</button>
    <button className="button">Middle</button>
    <button className="button">Bottom</button>
  </div>
</div>

```html
<div class="button-group button-group--vertical button-group--attached">
  <button class="button">Top</button>
  <button class="button">Middle</button>
  <button class="button">Bottom</button>
</div>
```

### Block Button Group

Use `.button-group--block` for full-width groups with equal-width buttons:

<div className="component-preview component-preview--column">
  <div className="button-group button-group--block">
    <button className="button">Equal</button>
    <button className="button">Width</button>
    <button className="button">Buttons</button>
  </div>
</div>

```html
<div class="button-group button-group--block">
  <button class="button">Equal</button>
  <button class="button">Width</button>
  <button class="button">Buttons</button>
</div>
```

## Combining Modifiers

Modifiers can be combined for custom styling:

<div className="component-preview component-preview--center">
  <button className="button button--success button--lg button--rounded">
    Complete Action
  </button>
  <button className="button button--danger button--xs button--circle">×</button>
</div>

<div className="component-preview component-preview--column">
  <button className="button button--outlined button--sm button--block">
    Full Width Secondary
  </button>
</div>

```html
<!-- Large, rounded, success button -->
<button class="button button--success button--lg button--rounded">
  Complete Action
</button>

<!-- Small, outlined, block button -->
<button class="button button--outlined button--sm button--block">
  Full Width Secondary
</button>

<!-- Extra small, danger, circle button -->
<button class="button button--danger button--xs button--circle">×</button>
```

## Accessibility

The button component follows accessibility best practices:

- **Focus-visible**: Clear 2px outline on keyboard focus
- **Disabled states**: Proper `pointer-events: none` and reduced opacity
- **Interactive feedback**: Hover and active states provide visual feedback

### Recommendations

1. Always provide meaningful text content or `aria-label` for icon-only buttons
2. Use `<button>` elements for actions, `<a>` elements for navigation
3. Avoid disabling buttons without providing context about why

<div className="component-preview component-preview--center">
  <button className="button button--circle" aria-label="Close dialog">×</button>
  <a href="#" className="button button--success">Sign Up Link</a>
</div>

```html
<!-- Good: Icon button with aria-label -->
<button class="button button--circle" aria-label="Close dialog">×</button>

<!-- Good: Link styled as button -->
<a href="/signup" class="button button--success">Sign Up</a>
```

## CSS Custom Properties

The button uses these CSS custom properties for theming:

| Property                      | Description                 |
| ----------------------------- | --------------------------- |
| `--color-primary`             | Primary button background   |
| `--color-primary-hover`       | Primary hover state         |
| `--color-secondary`           | Secondary button background |
| `--color-secondary-hover`     | Secondary hover state       |
| `--color-success`             | Success button color        |
| `--color-warning`             | Warning button color        |
| `--color-error`               | Danger button color         |
| `--space-xs` to `--space-2xl` | Spacing scale               |
| `--text-xs` to `--text-xl`    | Font sizes                  |
