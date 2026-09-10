# Tentwenty — Shopify Developer — Test Assignment

A customized **Shopify Dawn theme** built for the TenTwenty developer test assignment. This project extends the Dawn base theme with custom sections, sliders, and UI enhancements tailored to modern e-commerce requirements.

---

## ?? Project Structure

```
+-- assets/          ? CSS, JS, SVG icons, and media files
+-- config/          ? Theme settings schema and data
+-- layout/          ? Root theme and password page layouts
+-- locales/         ? Internationalization strings
+-- sections/        ? Theme sections (custom + extended Dawn sections)
+-- snippets/        ? Reusable Liquid partials
+-- templates/       ? Page templates (JSON + Liquid)
```

---

## ? Custom Sections Added

### 1. `image-shuffle-slider.liquid` — TenTwenty Tilted Cards Drag Slider
A fully custom, pixel-perfect interactive slider built with **pure CSS + Vanilla JS** (no external libraries).

**Features:**
- Tilted card layout with left/right independent rotation controls
- Draggable card interaction
- Fully customizable via Shopify Theme Editor:
  - Card width, gap, background color, padding
  - Title size, weight, color, alignment
  - Side card scale and rotation (left/right independently)
  - Header gap and max width
- Responsive and theme-editor compatible (`shopify_attributes`)

**File:** `sections/image-shuffle-slider.liquid`

---

### 2. `test-slider.liquid` — Custom Fullscreen Slider
A Shopify OS 2.0-compatible fullscreen slider with layered cover animation.

**Features:**
- Fully configurable via Theme Editor:
  - Autoplay with custom delay
  - Transition speed and animation type
  - Easing function selection
  - Pause on hover, loop toggle
  - Desktop / tablet / mobile height (vh)
  - Overlay opacity
  - Content width and next-button position
- CSS custom properties (`--cs-*`) for responsive design
- Accessible markup (`aria-label`, keyboard support via `tabindex`)
- Start index configurable from Theme Editor

**File:** `sections/test-slider.liquid`

---

## ??? Standard Dawn Sections (Extended)

| Section | Description |
|---|---|
| `header.liquid` | Site header with mega menu, cart, and search |
| `footer.liquid` | Site footer with social links and navigation |
| `featured-product.liquid` | Full product display section |
| `featured-collection.liquid` | Collection product grid |
| `image-banner.liquid` | Hero image banner |
| `image-with-text.liquid` | Split image + text layout |
| `slideshow.liquid` | Dawn native slideshow |
| `collage.liquid` | Image collage / mosaic |
| `multicolumn.liquid` | Multi-column content section |
| `multirow.liquid` | Multi-row content section |
| `rich-text.liquid` | Rich text editor section |
| `newsletter.liquid` | Email newsletter signup |
| `email-signup-banner.liquid` | Full-width email capture banner |
| `featured-blog.liquid` | Blog post highlights |
| `collapsible-content.liquid` | FAQ / accordion content |
| `collection-list.liquid` | Collection listing grid |
| `video.liquid` | Embedded video section |
| `contact-form.liquid` | Contact form section |
| `announcement-bar.liquid` | Top announcement bar |
| `predictive-search.liquid` | Predictive search results |
| `related-products.liquid` | Related products carousel |

---

## ?? Snippets

- `card-product.liquid` — Product card UI component
- `card-collection.liquid` — Collection card UI component
- `article-card.liquid` — Blog article card
- `facets.liquid` — Collection filter and sort UI
- `cart-drawer.liquid` — Side cart drawer
- `header-drawer.liquid` — Mobile navigation drawer
- `header-mega-menu.liquid` — Desktop mega menu
- `product-media-gallery.liquid` — Product image gallery
- `product-variant-picker.liquid` — Variant selector UI
- `price.liquid` — Price display with sale logic
- `buy-buttons.liquid` — Add to cart / buy now buttons
- `pagination.liquid` — Page navigation
- `social-icons.liquid` — Social media icon links
- `swatch.liquid` / `swatch-input.liquid` — Color/variant swatches

---

## ?? Assets

**JavaScript:** `global.js`, `cart.js`, `product-info.js`, `facets.js`, `predictive-search.js`, `quick-add.js`, `animations.js`, `magnify.js`, `standard-actions-override.js`

**CSS:** `base.css`, component stylesheets (`component-*.css`), section stylesheets (`section-*.css`), `mask-blobs.css`

**Icons:** 80+ SVG icons for cart, account, social networks, product features, and UI controls

---

## ??? Configuration

- `config/settings_schema.json` — Theme Editor settings definitions
- `config/settings_data.json` — Saved theme customizations
- `layout/theme.liquid` — Main HTML layout
- `layout/password.liquid` — Coming-soon page layout

---

## ?? Templates

| Template | Description |
|---|---|
| `index.json` | Homepage |
| `product.json` | Product detail page |
| `collection.json` | Collection listing page |
| `cart.json` | Cart page |
| `blog.json` | Blog listing |
| `article.json` | Blog post |
| `page.json` | Generic page |
| `page.contact.json` | Contact page |
| `search.json` | Search results |
| `404.json` | Not found page |
| `password.json` | Password / coming soon page |
| `list-collections.json` | All collections page |
| `gift_card.liquid` | Gift card template |

---

## ?? Getting Started

### Prerequisites
- A Shopify store (development or production)
- [Shopify CLI](https://shopify.dev/docs/themes/tools/cli) installed

### Deploy via Shopify CLI

```bash
# Authenticate with Shopify
shopify theme dev --store your-store.myshopify.com

# Push theme to your store
shopify theme push

# Preview in development
shopify theme dev
```

### Upload via Shopify Admin
1. Go to **Online Store ? Themes**
2. Click **Add theme ? Upload zip file**
3. Zip this folder and upload

---

## ????? Developer

**Virendra Solanki**
Shopify Developer — TenTwenty Test Assignment
Store: `virendra-solanki-pwomrqrh.myshopify.com`

---

## ?? Notes

- Based on Shopify open-source **Dawn** theme
- Custom sections are self-contained with inline CSS/JS — no build step required
- Compatible with **Shopify Online Store 2.0**
- All custom settings exposed via Theme Editor (`settings_schema`)
