# Arachnoscript

A spider-based display font, hand-drawn and built into a working typeface.
`a–z` and `A–Z` are the same glyph; digits `0–9` included.

## Pages
- **`index.html`** — mobile on-screen keypad: tap the glyph keys to write (no
  phone keyboard pops up). Copy / Clear, and a Latin readout toggle.
- **`tester.html`** — type anything and see it render live; switch font / size /
  tracking / background.
- **`specimen.html`** — reference sheet of every glyph plus the `@font-face` CSS.

## Fonts (`assets/`)
- `Arachnoscript-Regular` — your glyphs only (letters + digits). Lightest;
  punctuation falls back to a system font.
- `ArachnoscriptText-Regular` — self-contained: your letters + digits with
  English punctuation/symbols built in.

Both ship as `.woff2` (web) and `.ttf` (fallback / desktop install).

## Use the font elsewhere
```css
@font-face {
  font-family: 'Arachnoscript';
  src: url('assets/Arachnoscript-Regular.woff2') format('woff2'),
       url('assets/Arachnoscript-Regular.ttf')   format('truetype');
  font-display: swap;
}
.arachno { font-family: 'Arachnoscript', system-ui, sans-serif; }
```

## Deploy (GitHub Pages)
Push these files to a repo, then **Settings → Pages → Build from a branch →
`main` / `/ (root)`**. The site goes live at
`https://<username>.github.io/<repo>/`.

Punctuation in `ArachnoscriptText` comes from DejaVu Sans (Bitstream Vera /
public-domain license).
