# KK Electrical website

Static website (plain HTML, CSS and JavaScript, no build step) for KK Electrical, Kempton Park.

```
kk-electrical/
  index.html        main website
  ads.html          social media ads + copy-paste captions
  css/style.css     website styles (colours at the top)
  css/ads.css       ad styles
  js/main.js        phone menu, scroll animation, WhatsApp form
  js/ads.js         "Copy caption" buttons
  images/           PUT YOUR PHOTOS HERE (see images/README.md for names and sizes)
```

## 1. Add pictures
Open `images/README.md`. Every picture slot in `index.html` is also marked with a
`>>> PICTURE <<<` comment showing the file name and recommended size.

## 2. Edit text and details
- Phone / WhatsApp / email: search `index.html`, `ads.html` and `js/main.js` for these four values: `072 126 1704`, `+27721261704`, `27721261704` and `kkchokoe@gmail.com`. Use Find and Replace so every spot changes.
- WhatsApp form number: `js/main.js`.
- Colours: top of `css/style.css` (`--blue` is the main brand colour).

## 3. Show the client on GitHub (free, via GitHub Pages)
1. Create a free account at github.com and click **New repository**. Name it e.g. `kk-electrical`. Keep it **Public** (free GitHub Pages needs a public repo on free accounts).
2. Click **uploading an existing file**, then drag in the CONTENTS of this folder (`index.html`, `ads.html`, and the `css`, `js`, `images` folders). Keep the folder structure. Click **Commit changes**.
3. Go to **Settings > Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io/kk-electrical/`. The ads page is at `.../ads.html`.
5. To update: edit or re-upload files in the repo; the site refreshes by itself in a minute or two.

Notes: the site is public, so anyone with the link can see it. Don't put anything private in the repo.
The ads page is a working page for you; you may prefer to leave `ads.html` out of what the client sees.

## 4. Moving to GoDaddy
Check what your GoDaddy plan is first, because the right route depends on it.

**Option A (simplest, keeps this design exactly): upload the files as they are.**
If you have GoDaddy Web Hosting (cPanel): open **File Manager > public_html** and upload everything (`index.html`, `css`, `js`, `images`). Point your domain at it. Use this if the client does not need to edit the site in WordPress.

**Option B: put it inside WordPress.**
WordPress does not run a plain HTML file as a theme, so the design has to be brought in. The least painful way:
1. Install a page-builder or blank-canvas option (for example Elementor with the "Canvas" template, or a "Blank page template" plugin) so the page has no theme header or footer.
2. Create a Page, add a **Custom HTML** block, and paste the body of `index.html` (everything between `<body>` and `</body>`, without the `<script>` line).
3. Paste the contents of `css/style.css` into **Appearance > Customize > Additional CSS** (it may clash with the theme's own styles, so check the page on a phone).
4. Upload photos in **Media > Add New** and change the `images/...` paths in the HTML to the full URLs WordPress gives you.
5. Menu toggle and scroll effects need `js/main.js`. Add it with a plugin like "WPCode" in the footer, or skip them.

Option B takes more adjusting. If the client wants to edit text and photos themselves, it is usually better to rebuild the same layout with the WordPress theme or builder and reuse the colours, wording and photos from this site.

GoDaddy's Managed WordPress plans can limit file access, so ask their support if you can't find File Manager or FTP.
