# SmartShoes — GitHub Pages storefront

A mobile-first static storefront for SmartShoes Pakistan. Product data lives in `js/products.js`; cart and wishlist use browser `localStorage`.

## Run locally

Because this is a static site, open it with any static server (recommended for consistent browser behavior):

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Select **Deploy from a branch**, choose `main` and `/ (root)`, then Save.
4. Wait for the Pages deployment and use the generated project URL.

All internal links are relative so the storefront works from a GitHub Pages project path. `404.html` is included at the published root.

## Safe configuration

- Replace the sample products and image URLs in `js/products.js` with approved catalog content.
- Replace contact/social links and policy copy with the real SmartShoes business details.
- Product prices, delivery charges, stock, and returns policies should be managed from the authoritative business system before launch.

## Backend requirements

This repository intentionally does **not** implement fake authentication, payment verification, order persistence, inventory, or email delivery. Connect checkout to a secure backend/serverless function or e-commerce provider before accepting real orders. Never commit payment private keys, database credentials, admin credentials, or other secrets to this repository. The online-payment UI is only a safe handoff placeholder; a server must create and verify provider sessions.

## Included routes

Home, Shop/category query views, Product details, Cart, Checkout, and 404 are implemented. The documentation links for support pages can be added as policy content becomes available; do not publish invented delivery, return, legal, or courier claims.
