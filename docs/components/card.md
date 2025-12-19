---
sidebar_label: "Card"
---

# Card

A flexible product card component designed to display content, images, and actions. It follows the BEM methodology and includes standard interaction states and modifiers.

## Anatomy

The `.card` component is structured with the following BEM elements:

- **`.card`**: The main container.
- **`.card__media`**: Container for the product image.
- **`.card__badge`**: Optional badge overlay (e.g., "NEW", "SALE").
- **`.card__body`**: The main content wrapper with fluid padding.
- **`.card__content`**: Holds the textual content.
- **`.card__title`**: Product title with line clamping.
- **`.card__rating`**: Star rating display.
- **`.card__price`**: Container for pricing (current and old).
- **`.card__actions`**: Footer area for buttons (pushed to bottom).

## Basic Usage

The standard product card includes an image, title, rating, price, and action button.

<div className="component-preview component-preview--center">
  <div style={{ width: '340px' }} >
    <article className="card">
      <div className="card__media">
        <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=800&q=80" alt="Watch" />
        <span className="card__badge">New</span>
      </div>
      <div className="card__body">
        <div className="card__content">
          <h3 className="card__title">Minimalist White Dial Watch</h3>
          <div className="card__rating">
            ★★★★☆ <span>(4.5)</span>
          </div>
          <div className="card__price">
            <span className="card__price-current">$129.00</span>
          </div>
        </div>
        <div className="card__actions">
          <button className="button button--primary card__button">Add to Cart</button>
        </div>
      </div>
    </article>
  </div>
</div>

```html
<article class="card">
  <div class="card__media">
    <img src="path/to/image.jpg" alt="Product Name" />
    <span class="card__badge">New</span>
  </div>
  <div class="card__body">
    <div class="card__content">
      <h3 class="card__title">Minimalist White Dial Watch</h3>
      <div class="card__rating">★★★★☆ <span>(4.5)</span></div>
      <div class="card__price">
        <span class="card__price-current">$129.00</span>
      </div>
    </div>
    <div class="card__actions">
      <button class="button button--primary card__button">Add to Cart</button>
    </div>
  </div>
</article>
```

## Variants

### Featured Card

Highlights the card with a primary border and more pronounced hover effects.

<div className="component-preview component-preview--center">
  <div style={{ width: '340px' }}>
    <article className="card card--featured">
      <div className="card__media">
        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=800&q=80" alt="Headphones" />
        <span className="card__badge">Best Seller</span>
      </div>
      <div className="card__body">
        <div className="card__content">
          <h3 className="card__title">Premium Noise-Canceling Headphones</h3>
          <div className="card__rating">
            ★★★★★ <span>(5.0)</span>
          </div>
          <div className="card__price">
            <span className="card__price-current">$299.00</span>
          </div>
        </div>
        <div className="card__actions">
          <button className="button button--primary card__button">Add to Cart</button>
        </div>
      </div>
    </article>
  </div>
</div>

```html
<article class="card card--featured">
  <!-- Content -->
</article>
```

### Sale Card

Uses error colors for the badge and price to indicate a discount.

<div className="component-preview component-preview--center">
  <div style={{ width: '340px' }}>
    <article className="card card--sale">
      <div className="card__media">
        <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=800&q=80" alt="Sneakers" />
        <span className="card__badge">-20%</span>
      </div>
      <div className="card__body">
        <div className="card__content">
          <h3 className="card__title">Urban Runner Sneakers</h3>
          <div className="card__rating">
            ★★★★☆ <span>(4.2)</span>
          </div>
          <div className="card__price">
            <span className="card__price-old">$120.00</span>
            <span className="card__price-current">$96.00</span>
          </div>
        </div>
        <div className="card__actions">
          <button className="button button--primary card__button">Add to Cart</button>
        </div>
      </div>
    </article>
  </div>
</div>

```html
<article class="card card--sale">
  <!-- ... -->
  <div class="card__price">
    <span class="card__price-old">$120.00</span>
    <span class="card__price-current">$96.00</span>
  </div>
  <!-- ... -->
</article>
```

### Sold Out

Applies a partially transparent overlay and disables the action button.

<div className="component-preview component-preview--center">
  <div style={{ width: '340px' }}>
    <article className="card card--sold-out">
      <div className="card__media">
        <img src="https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=800&q=80" alt="Bag" />
      </div>
      <div className="card__body">
        <div className="card__content">
          <h3 className="card__title">Limited Edition Travel Bag</h3>
           <div className="card__rating">
            ★★★★★ <span>(5.0)</span>
          </div>
          <div className="card__price">
            <span className="card__price-current">$150.00</span>
          </div>
        </div>
        <div className="card__actions">
          <button className="button button--primary card__button" disabled>Out of Stock</button>
        </div>
      </div>
    </article>
  </div>
</div>

```html
<article class="card card--sold-out">
  <!-- Image overlay is handled via CSS -->
  <button class="button button--primary card__button" disabled>
    Out of Stock
  </button>
</article>
```

## States

### Loading State

Applies a skeleton loading animation to the media area and hides the image.

<div className="component-preview component-preview--center">
  <div style={{ width: '340px' }}>
    <article className="card is-loading">
      <div className="card__media"></div>
      <div className="card__body">
        <div className="card__content">
          <h3 className="card__title">Loading Product...</h3>
        </div>
      </div>
    </article>
  </div>
</div>

```html
<article class="card is-loading">
  <!-- ... -->
</article>
```

### Selected State

Adds a highlight ring and primary border color.

<div className="component-preview component-preview--center">
  <div style={{ width: '340px' }}>
    <article className="card is-selected">
     <div className="card__body">
        <h3 className="card__title">Selected Item</h3>
        <p>This card is currently selected.</p>
      </div>
    </article>
  </div>
</div>

## Grid Layout Integration

The card component is designed to work seamlessly with the grid system. Because `.card` has `height: 100%`, it will automatically stretch to match the height of other cards in the same row.

### Responsive Grid Example

This example demonstrates a 3-column grid layout (spanning 1 column on mobile, 2 on medium screens, and 3 on large screens).

<div className="component-preview">
  <div className="grid">
    <div className="col-12 col-md-6 col-lg-4">
      <article className="card">
        <div className="card__media">
           <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=800&q=80" alt="Product" />
        </div>
        <div className="card__body">
          <h3 className="card__title">Short Title</h3>
          <div className="card__actions">
             <button className="button button--outline card__button">View</button>
          </div>
        </div>
      </article>
    </div>
    <div className="col-12 col-md-6 col-lg-4">
      <article className="card">
         <div className="card__media">
           <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=800&q=80" alt="Product" />
        </div>
        <div className="card__body">
          <h3 className="card__title">A Much Longer Product Title That Might Span Two Lines to Demonstrate Height Matching</h3>
          <div className="card__actions">
             <button className="button button--outline card__button">View</button>
          </div>
        </div>
      </article>
    </div>
     <div className="col-12 col-md-6 col-lg-4">
      <article className="card card--sale">
         <div className="card__media">
           <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=800&q=80" alt="Product" />
           <span className="card__badge">-15%</span>
        </div>
        <div className="card__body">
          <h3 className="card__title">Another Product</h3>
          <p>Extra content to push the height further down.</p>
          <div className="card__actions">
             <button className="button button--outline card__button">View</button>
          </div>
        </div>
      </article>
    </div>
  </div>
</div>

```html
<div class="grid">
  <!-- Card 1 -->
  <div class="col-12 col-md-6 col-lg-4">
    <article class="card">...</article>
  </div>

  <!-- Card 2 -->
  <div class="col-12 col-md-6 col-lg-4">
    <article class="card">...</article>
  </div>

  <!-- Card 3 -->
  <div class="col-12 col-md-6 col-lg-4">
    <article class="card">...</article>
  </div>
</div>
```
