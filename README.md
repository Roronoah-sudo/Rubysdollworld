# Ruby's Doll World

The storefront website for Ruby's Doll World: glittery, glam doll outfits and dollhouses, handmade by Glamom.

It's a static site (plain HTML, CSS and JavaScript), so there's no build step and nothing to install.

## Project structure

```
index.html          The page
css/styles.css      All styling, colors and fonts
js/main.js          Products, dollhouses, videos, gallery and the cart
assets/             Images used by the site (logo, wordmark, silhouette, stars, glitter texture)
assets/brand/       Full-size transparent PNG logo kit
.nojekyll           Tells GitHub Pages to serve files as-is
```

## Preview locally

Open `index.html` in a browser, or run a tiny local server from this folder:

```
python3 -m http.server 8000
```

Then go to http://localhost:8000.

## Publish with GitHub Pages

1. Create a new repository on GitHub (for example `rubys-doll-world`).
2. Upload these files, or push them:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/rubys-doll-world.git
   git push -u origin main
   ```
3. In the repository, go to **Settings > Pages**, set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, and save.
4. The site will be live at `https://YOUR-USERNAME.github.io/rubys-doll-world/` within a minute or two.

To use a custom domain like `rubysdollworld.com`, add it under **Settings > Pages > Custom domain** and point your domain's DNS at GitHub Pages.

## Editing content

Everything sold or shown on the page lives at the top of `js/main.js`:

- `outfits` holds name, category, price, colors and description for each outfit
- `houses` holds the dollhouses, with price, number of floors and specs
- `videos` holds the YouTube list titles
- `gallery` holds the "Already made" tiles

Prices, names and descriptions there are placeholders.

## Placeholders still to replace

- **YouTube:** The link `https://www.youtube.com/@RubysDollWorld` is a placeholder. Search `RubysDollWorld` in `index.html` and `js/main.js` and replace it with the real channel. To show a real video, swap the `.player` block in `index.html` for the YouTube embed iframe.
- **Email:** `hello@rubysdollworld.com` is a placeholder. Search and replace it in `index.html` and `js/main.js`.
- **Product images:** Outfits and dollhouses use drawn illustrations. Add photos to `assets/` and they can replace the illustrations.
- **Gallery and Glamom photo:** The tiles and the arched portrait say "Photo soon" or "Glamom's photo goes here."
- **Checkout:** The cart works and saves in the browser, but checkout only shows a message. GitHub Pages can't process payments, so connect Stripe Payment Links, Shopify Buy Buttons or Square when you're ready to sell.
- **Shipping and Returns** footer links point to `#` until those pages exist.
