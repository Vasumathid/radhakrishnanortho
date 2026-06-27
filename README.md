# International Ortho Care — Website

A complete, animated, SEO-ready website for **Dr. Radhakrishnan's International Ortho Care** (Vadapalani, Chennai). Pure HTML/CSS/JS — **no build step, no npm install needed.** Works the moment you open it.

## 📁 What's inside

```
.
├── index.html        Homepage (hero, specialities, recovery timeline, doctor, testimonials)
├── about.html        Full doctor profile & clinic philosophy
├── services.html     6 detailed speciality sections (joint replacement, sports injury, spine, arthritis, deformity, trauma)
├── gallery.html      Clinic photos + all patient reviews
├── contact.html       Booking form, map, FAQ, both clinic locations
├── css/style.css     Full design system (colors, type, animations)
├── js/main.js        Scroll reveals, mobile nav, FAQ accordion, counters
└── README.md         You are here
```

## 🚀 Push to GitHub (copy-paste, in order)

Open a terminal inside this folder and run:

```bash
git init
git add .
git commit -m "Initial site: International Ortho Care"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

Replace `YOUR-USERNAME/YOUR-REPO-NAME` with your actual repo path. If you haven't created the repo yet, do that first at **github.com/new** (don't initialize it with a README — leave it empty, then run the commands above).

## 🌐 Make it live for free — GitHub Pages

1. In your GitHub repo, go to **Settings → Pages**
2. Under "Build and deployment" → **Source**, select **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)` → **Save**
4. Wait ~1 minute, then your site is live at:
   `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

No build tools, no Node, no config files needed — it's static HTML and goes live as-is.

## 🖥️ Run it locally (optional, before pushing)

You don't need anything installed to _view_ the site — just double-click `index.html` and it opens in your browser.

To run it through a local server (recommended, so relative links behave exactly like production):

```bash
# Python (already on most systems)
python3 -m http.server 8000
# then open http://localhost:8000
```

## ✏️ Before going live — replace these placeholders

| What                                                 | Where                                                  | Replace with                                                                  |
| ---------------------------------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------------------- |
| Phone number `+91 81244 56789`                       | All pages (header, footer, WhatsApp links, sticky CTA) | Actual clinic contact number                                                  |
| Kotturpuram address                                  | `contact.html`                                         | Confirm/replace with real second-clinic address                               |
| Google Map embed                                     | `contact.html` (`<iframe>` in `.map-embed`)            | Get the real embed link from Google Maps → Share → Embed a map                |
| Domain in `<link rel="canonical">` and `og:url` tags | All pages                                              | Your actual domain once you have one                                          |
| Clinic photos                                        | `gallery.html`                                         | Currently uses illustrated SVG placeholders — swap in real photos (see below) |

## 🖼️ Adding real photos

The gallery currently uses line-art SVG placeholders so the site works with zero image files. To add real photos:

1. Put image files in the empty `images/` folder (create it if needed) — e.g. `images/reception.jpg`
2. In `gallery.html`, replace a `<div class="g-tile">...</div>` block with:
   ```html
   <div
     class="g-tile"
     style="background-image:url('images/reception.jpg'); background-size:cover; background-position:center;"
   >
     <div class="g-label">Reception &amp; waiting area</div>
   </div>
   ```
3. Repeat for each tile.

## 🔍 SEO already built in

- Per-page `<title>` and `<meta description>` tailored to search intent (e.g. "knee replacement Chennai", "orthopaedic doctor Vadapalani")
- `Physician` structured data (JSON-LD) on the homepage — eligible for Google's rich result panels (ratings, hours, address)
- Semantic heading hierarchy (single H1 per page, logical H2/H3 nesting)
- Fast-loading: no frameworks, no render-blocking JS, system fonts fallback
- Mobile-first responsive layout with sticky call-to-book bar on phones

## ♿ Accessibility

- Skip-to-content link on every page
- Visible focus states on all interactive elements
- `prefers-reduced-motion` respected — animations disable for users who request it
- Sufficient color contrast across the navy/bone/clay palette

## 🎨 Design system reference

| Token          | Hex       | Use                                  |
| -------------- | --------- | ------------------------------------ |
| Navy           | `#0F2A3D` | Headers, primary text, dark sections |
| Bone           | `#F7F4EE` | Page background                      |
| Clay           | `#C77B3D` | Primary buttons, accents, links      |
| Recovery green | `#2E6B4F` | Success/positive indicators, icons   |

Fonts: **Fraunces** (headings), **Inter** (body), **IBM Plex Mono** (stats, labels, eyebrow text) — all loaded from Google Fonts CDN, no local font files required.

---

Built for Dr. Radhakrishnan's International Ortho Care, Vadapalani, Chennai.
