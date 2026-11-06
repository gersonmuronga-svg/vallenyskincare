# Valleny Skincare — vallenyskincare.com

Single-page shop website: products & prices, product detail pop-ups, a draggable before/after slider, reviews, FAQ, and a bag that sends the order to WhatsApp.

## Editing content
Everything editable is at the top of the `<script>` in `index.html`, between the `EDIT EVERYTHING HERE` and `END OF EDITABLE SECTION` markers:

- `SHOP` — WhatsApp number (country code, no + or spaces, e.g. `264811234567`), phone, email, Instagram, hero/about photos
- `PRODUCTS` — name, category, price, size, badge, descriptions, image
- `RESULTS` — before/after cases (`before` / `after` image paths, linked products)
- `REVIEWS` — client testimonials

## Images
- Product photos → `images/products/` (square-ish, ~1000×1050 px, JPG/WebP under 300 KB)
- Before/after → `images/results/` (both photos same size and framing, ~1200×1000 px)
- Then set e.g. `img: "images/products/glow-serum.jpg"`. Empty `""` shows the built-in placeholder.

## Publishing on GitHub Pages
1. Create the repo and upload all files (keep `CNAME` in the root).
2. Settings → Pages → Source: *Deploy from a branch* → `main` / root.
3. Custom domain: `vallenyskincare.com`, then tick **Enforce HTTPS** once the certificate is issued.
4. At the domain registrar, add DNS records:
   - `A` records for `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - `CNAME` for `www` → `<your-github-username>.github.io`

Hosting: GitHub Pages (public repo — only invited collaborators can change the code). DNS is on Cloudflare.
