---
sidebar_position: 1
sidebar_label: "Grid System"
---

# Grid System

A comprehensive layout system featuring a 12-column grid, containers, flexbox utilities, and vertical stacks.

## Container

The `.container` class is the main content wrapper. It provides responsive max-widths and automatic centering.

| Class                | Description                                                                        |
| :------------------- | :--------------------------------------------------------------------------------- |
| `.container`         | Default fluid-responsive container                                                 |
| `.container--fluid`  | 100% width container                                                               |
| `.container--narrow` | Narrow container for blog posts/articles (max-width constrained on larger screens) |

### Responsive Max-Widths

The `.container` adapts its maximum width at specific breakpoints:

| Breakpoint | Value    | Max-Width |
| :--------- | :------- | :-------- |
| `sm`       | ≥ 576px  | 540px     |
| `md`       | ≥ 768px  | 720px     |
| `lg`       | ≥ 1024px | 960px     |
| `xl`       | ≥ 1280px | 1140px    |
| `xxl`      | ≥ 1536px | 1320px    |

```html
<div class="container">
  <!-- Content constrained to max-widths above -->
</div>
```

## Grid vs. Flex

The framework provides two main ways to handle layout:

- **Grid (`.grid`)**: Best for two-dimensional layouts where you need to align items in rows and columns simultaneously. It uses a strict 12-column grid system.
- **Flex (`.flex`)**: Best for one-dimensional layouts (a row OR a column). It offers more fluid sizing and is ideal for aligning a few items (like navbars, media objects, or toolbars).

## Grid System

The `.grid` class initiates a responsive 12-column CSS Grid layout.

### Basic 12-Column Grid

Use `.col-{1-12}` classes to define column spans. By default, columns are applied at all breakpoints.

<div className="component-preview">
  <div className="grid grid--gap-sm">
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-1" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>1</div>
    <div className="col-4" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>4</div>
    <div className="col-4" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>4</div>
    <div className="col-4" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>4</div>
    <div className="col-6" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>6</div>
    <div className="col-6" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>6</div>

  </div>
</div>

```html
<div class="grid">
  <div class="col-4">Column 4</div>
  <div class="col-4">Column 4</div>
  <div class="col-4">Column 4</div>
</div>
```

### Grid Alignment

You can control the alignment of items within the grid tracks (horizontal and vertical center).

| Modifier        | Description                           |
| :-------------- | :------------------------------------ |
| `.grid--start`  | Align items to start (top-left)       |
| `.grid--center` | Align items to center (middle-center) |
| `.grid--end`    | Align items to end (bottom-right)     |

<div className="component-preview">
  <div className="grid grid--center" style={{height: '150px', background: '#f9fafb'}}>
    <div className="col-4" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>Centered Item</div>
    <div className="col-4" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>Centered Item</div>
     <div className="col-4" style={{background: '#e5e7eb', padding: '1rem', textAlign: 'center'}}>Centered Item</div>
    
  </div>
</div>

```html
<div class="grid grid--center" style="min-height: 200px;">
  <div class="col-4">Centered Vertically & Horizontally</div>
  <div class="col-4">Centered Vertically & Horizontally</div>
  <div class="col-4">Centered Vertically & Horizontally</div>
</div>
```

### Gap Modifiers

Control the gap between grid text items.

| Modifier          | Description         |
| :---------------- | :------------------ |
| `.grid--gap-xs`   | Extra small gap     |
| `.grid--gap-sm`   | Small gap           |
| `.grid--gap-md`   | Medium gap          |
| `.grid--gap-lg`   | Large gap (default) |
| `.grid--gap-xl`   | Extra large gap     |
| `.grid--gap-none` | No gap              |

### Responsive Columns

The grid system supports responsive column classes using standard breakpoints:
`sm` (≥576px), `md` (≥768px), `lg` (≥1024px), `xl` (≥1280px), `xxl` (≥1536px).

<div className="component-preview">
  <div className="grid">
    <div className="col-12 col-md-6 col-lg-3" style={{background: '#e5e7eb', padding: '1rem'}}>
      <strong>Box 1</strong><br/>
      12 cols (mobile)<br/>
      6 cols (tablet)<br/>
      3 cols (desktop)
    </div>
    <div className="col-12 col-md-6 col-lg-3" style={{background: '#e5e7eb', padding: '1rem'}}>
      <strong>Box 2</strong>
    </div>
    <div className="col-12 col-md-6 col-lg-3" style={{background: '#e5e7eb', padding: '1rem'}}>
      <strong>Box 3</strong>
    </div>
    <div className="col-12 col-md-6 col-lg-3" style={{background: '#e5e7eb', padding: '1rem'}}>
      <strong>Box 4</strong>
    </div>
  </div>
</div>

```html
<div class="grid">
  <!-- Full width on mobile, half width on tablet, quarter width on desktop -->
  <div class="col-12 col-md-6 col-lg-3">...</div>
  <div class="col-12 col-md-6 col-lg-3">...</div>
  <div class="col-12 col-md-6 col-lg-3">...</div>
  <div class="col-12 col-md-6 col-lg-3">...</div>
</div>
```

## Flex Utility

The `.flex` class enables flexible layouts.

### Alignment & Justification

Modifiers control alignment and justification of flex items.

<div className="component-preview component-preview--column">
  
  <strong>Justify Start (Default)</strong>
  <div className="flex flex--justify-start" style={{background: '#f3f4f6', padding: '1rem', marginBottom: '1rem'}}>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>1</div>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>2</div>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>3</div>
  </div>

<strong>Justify Center</strong>

  <div className="flex flex--justify-center" style={{background: '#f3f4f6', padding: '1rem', marginBottom: '1rem'}}>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>1</div>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>2</div>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>3</div>
  </div>

<strong>Justify Between</strong>

  <div className="flex flex--justify-between" style={{background: '#f3f4f6', padding: '1rem'}}>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>Start</div>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>Between</div>
    <div style={{background: '#3b82f6', color: 'white', padding: '0.5rem 1rem'}}>End</div>
  </div>

</div>

```html
<!-- Justified Start -->
<div class="flex flex--justify-start">...</div>

<!-- Justified Center -->
<div class="flex flex--justify-center">...</div>

<!-- Justified Between -->
<div class="flex flex--justify-between">...</div>
```

**Available Modifiers:**

- **Direction:** `flex--row`, `flex--col`, `flex--row-reverse`, `flex--col-reverse`
- **Wrap:** `flex--wrap`, `flex--nowrap`
- **Justify:** `flex--justify-start`, `flex--justify-center`, `flex--justify-end`, `flex--justify-between`, `flex--justify-around`, `flex--justify-evenly`
- **Align:** `flex--items-start`, `flex--items-center`, `flex--items-end`, `flex--items-baseline`, `flex--items-stretch`
- **Gap:** `flex--gap-xs` through `flex--gap-xl`, and `flex--gap-none`

### Flex Items

Use `flex__item` with modifiers to control individual item behavior.

- `flex__item--grow`: `flex-grow: 1`
- `flex__item--shrink`: `flex-shrink: 1`
- `flex__item--no-grow`: `flex-grow: 0`
- `flex__item--no-shrink`: `flex-shrink: 0`

## Stack

The `.stack` class is a vertical flex container designed for spacing out content blocks vertically.

<div className="component-preview">
  <div className="stack stack--lg" style={{background: '#f9fafb', padding: '1rem'}}>
    <div style={{background: 'white', padding: '1rem', border: '1px solid #e5e7eb'}}>Block 1</div>
    <div style={{background: 'white', padding: '1rem', border: '1px solid #e5e7eb'}}>Block 2 (spaced by lg gap)</div>
    <div style={{background: 'white', padding: '1rem', border: '1px solid #e5e7eb'}}>Block 3</div>
  </div>
</div>

```html
<div class="stack stack--lg">
  <div>Block 1</div>
  <div>Block 2</div>
  <div>Block 3</div>
</div>
```

## Section

The `.section` class provides fluid vertical padding for clear page segmentation. The padding scales fluidly between viewports to maintain appropriate spacing.

| Modifier              | Description                                                    |
| :-------------------- | :------------------------------------------------------------- |
| `.section`            | Default fluid padding (e.g., 32px on mobile → 96px on desktop) |
| `.section--sm`        | Smaller static padding (e.g., 24px)                            |
| `.section--no-top`    | Remove top padding                                             |
| `.section--no-bottom` | Remove bottom padding                                          |

<div className="component-preview component-preview--column" style={{padding: 0}}>
  <div className="section section--sm" style={{background: '#e0f2fe', borderBottom: '1px dashed #0ea5e9'}}>
    <div className="container" style={{background: 'rgba(255,255,255,0.5)', textAlign: 'center'}}>
      Section Small (Static)
    </div>
  </div>
  <div className="section" style={{background: '#f0f9ff'}}>
    <div className="container" style={{background: 'rgba(255,255,255,0.5)', textAlign: 'center'}}>
      Section Default (Fluid Padding)
    </div>
  </div>
</div>

```html
<!-- Main Page Section -->
<section class="section">
  <div class="container">
    <h2>Section Title</h2>
    <p>Content...</p>
  </div>
</section>

<!-- Compact Section -->
<section class="section section--sm">
  <div class="container">...</div>
</section>
```
