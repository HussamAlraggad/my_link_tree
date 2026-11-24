# Hussam Alraggad — Links

A one-page contact sheet for Hussam Alraggad's public channels. Warm paper, ink, the colored character mark, and six numbered frames.

**Live URL (once Pages is enabled):** https://hussamalraggad.github.io/my_link_tree/

## Stack

- HTML and CSS only, plus a JSON-LD metadata block. No executable JavaScript, no framework, no build step, no package manager.
- No third-party requests, analytics, cookies, or tracking pixels.
- One self-hosted font subset, one colored mark, one black watermark, one favicon.
- About 52 KB transferred on first load; under 100 KB including the social preview, which the page never loads.

## Files

```
index.html                     page content and metadata
styles.css                     the complete design system
assets/fonts/archivo-subset.woff2   30 KB Latin variable subset
assets/fonts/OFL.txt           Archivo's SIL Open Font License
assets/mark/color-512.avif     the colored mark in the portrait
assets/mark/color-256.webp     WebP fallback for the portrait
assets/mark/black-256.avif     the very faint background watermarks
assets/icons/favicon-32.png    the tab icon
assets/og.jpg                  1200x630 social preview, not loaded by the page
logo/                          original 500x500 SVGs — source only, never loaded by the page
```

## Edit the links

Open `index.html` and find the six `<a class="frame">` blocks. Each block has:

- `href` — the destination. Email uses `mailto:`; the rest open in a new tab.
- `aria-label` — the spoken label, including “opens in a new tab” where true.
- the visible frame number, kind, label, and handle.

Keep the `aria-label` and the visible text in sync. The first frame is `.is-primary` and should remain the email if email stays the preferred action.

The grid is tuned for six frames: 2 columns × 3 rows on desktop, 1 column on mobile. If you add a seventh frame, adjust the bottom-border rules (`.frame:nth-child(n+5)` and the mobile overrides in `styles.css`) so the final row closes cleanly.

If a handle changes, also update the `sameAs` array in the Person JSON-LD in `index.html`.

## Update the metadata

All absolute URLs point at `https://hussamalraggad.github.io/my_link_tree/`. If the repository name or domain changes, update:

- `<link rel="canonical">`
- `og:url`, `og:image`, and `twitter:image`
- the JSON-LD `url`
- `sitemap.xml`
- `robots.txt`

`assets/og.jpg` is a 1200×630 still of the page. Regenerate it if the design changes.

## Run locally

There is no build step. From the repository root:

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173/`.

## Deploy

The site is designed for GitHub Pages from the repository root:

1. Commit and push `main`.
2. In the repository, open **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. The site publishes at `https://hussamalraggad.github.io/my_link_tree/`.

`.nojekyll` is included so Pages serves the files as they are. No workflow, no build, no `node_modules`.

## Assets and font

The supplied logo SVGs are 500×500 but each is 300–390 KB because they embed a high-resolution PNG. They remain in `logo/` as source. The page loads only optimized derivatives:

- the colored mark as AVIF with a WebP fallback;
- the black mark as a 4.6 KB AVIF used at 3.5% opacity for the watermarks;
- a 32px PNG favicon built from the colored mark on the paper ground.

Archivo is subset to the Latin range and self-hosted. Its OFL license is in `assets/fonts/OFL.txt`.

## Accessibility

- Semantic `main`, one `h1`, a skip link, and a real list of links.
- Every external link names its destination and the new-tab behavior in `aria-label`.
- Focus is a 2px brown outline, inset on frames.
- Functional text is 11px or larger; the footer metadata is 10px; decorative portrait codes are `aria-hidden`.
- The page has no client-side behavior code; the only script element is JSON-LD metadata.
- Reduced-motion users get no entrance animation or transitions.
- The watermark images are decorative and hidden from assistive technology; the mark has empty alt because the name is text beside it.
- Hover is never required: every link, the primary tag, and all content are visible at rest.

## Brand

The character face — round glasses, large nose, handlebar mustache — is the mark. The colored version leads the page; the black version is the paper watermark; the white version remains in `logo/` for dark surfaces but is not used here. The visible kicker uses the public role **Software engineer / AI software**.
