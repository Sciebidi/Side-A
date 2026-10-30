# SIDE A

A static vinyl marketplace interface. Open home.html directly, or publish this folder as the document root. No build step, package installation, external fonts, or runtime dependencies are required. index.html continues to redirect to home.html.

## Files

- css/site.css — design tokens, textured cream paper, typography, navigation, artwork, cards, forms, footer, and responsive layouts.
- css/album-detail.css — album-specific product, tracklist, specification, and related-record layouts.
- css/motion.css — restrained interaction transitions and reduced-motion support.
- css/cart.css — responsive cart, custom-vinyl builder, and checkout components.
- js/catalog.js — the original nine-record catalog, including unchanged metadata and image filenames.
- js/cart.js — shared localStorage cart, catalog quick-add actions, and navigation count.
- js/cart-page.js — cart rendering, quantity controls, removal, clear, and custom edit links.
- js/custom-vinyl.js — independent vinyl configurations, artwork preview, track editing, ordering, and capacity guidance.
- js/checkout.js — customer validation, order review, and local-only confirmation preview.
- js/home.js — manual featured-record carousel with keyboard and touch controls.
- js/collection.js — accessible search, genre filtering, result count, and empty state.
- js/forms.js — contact form validation and local message preview.
- js/motion.js — mobile navigation only; native page navigation is preserved.

The cart is stored in the browser under `sideA.cart.v1`. Catalog copies merge by record; each custom configuration stays independent and can be edited from the cart. Custom artwork is resized before storage. Legacy album links such as `purchase.html?album=cinema` still work and add that record to the cart.

The catalog also appears in static collection and album markup. If catalog information changes, update js/catalog.js and the corresponding HTML together. Existing catalog information was preserved as supplied.

## Cart and checkout

Checkout is a frontend-only order review. Customer details are not submitted or saved, no order is sent, and no payment processing exists. Catalog subtotal is calculated from the displayed prices; shipping is a placeholder, and custom-vinyl pricing and availability require confirmation. Track capacity counts are planning guidance, not manufacturing specifications. Connect a backend and payment provider before accepting orders. The contact form also remains a local preview; existing email and Instagram links remain available.

## Verification

The project-level ../qa folder contains the pre-edit audit, layout results, interaction results, original-asset hashes, and full-page screenshots. All 14 content pages were checked at 1920, 1440, 1024, 768, and 390 pixels in Chromium. The original 15 HTML, 2 CSS, and 1 JavaScript source files are backed up in ../.side-a-originals.

Publish only the contents of this Vinyl folder. Keep albums, css, js, and all original image files in place.
