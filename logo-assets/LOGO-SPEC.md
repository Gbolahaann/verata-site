# Verata logo — "The Ledger" (option 1d)

Lowercase mono wordmark with a square full stop. The statement ends verified.

## Construction
- Wordmark: the string `verata` — always lowercase, never "Verata"
- Font: Geist Mono, weight 500, letter-spacing -0.06em
  - Google Fonts: https://fonts.google.com/specimen/Geist+Mono
  - CSS import: `@import url('https://fonts.googleapis.com/css2?family=Geist+Mono:wght@400..600&display=swap');`
  - Fallback stack: `'Geist Mono', ui-monospace, 'SF Mono', Menlo, monospace`
- The square (full stop):
  - Size: 0.16em × 0.16em (relative to wordmark font size)
  - Gap after final "a": 0.14em (margin-left)
  - Sits ON the baseline (bottom-aligned with letterforms), sharp corners — never rounded
  - Never scale, recolor, or animate the square independently

## Color
- Light backgrounds: text #17151C, square #46237A (brand violet)
- Dark backgrounds (#17151C): text #FAFAF9, square #A78BFA (light violet)
- One-color contexts (embossing, fax, stamps): everything one color, square included

## HTML/CSS (preferred — renders crisp at any size)
```html
<span class="verata-logo">verata<i></i></span>
```
```css
.verata-logo {
  font-family: 'Geist Mono', ui-monospace, 'SF Mono', Menlo, monospace;
  font-weight: 500;
  letter-spacing: -0.06em;
  color: #17151C;
  line-height: 1;
}
.verata-logo i {
  display: inline-block;
  width: 0.16em; height: 0.16em;
  background: #46237A;
  margin-left: 0.14em;
}
/* Dark-mode variant */
.dark .verata-logo { color: #FAFAF9; }
.dark .verata-logo i { background: #A78BFA; }
```
Size by setting `font-size` on `.verata-logo`; everything scales with it.

## Sizes
- Nav: 20–22px font-size
- Footer: 18–20px
- Minimum: 14px (below this, drop the square and use plain `verata`)
- Favicon / avatar: lone `v` + square (see verata-favicon.svg)

## Clear space
Keep a margin of 1× the square's width (0.16em) × 4 on all sides — i.e. roughly the height of the letter "v" around the mark.

## Don'ts
- No uppercase, no italic, no bold (weight stays 500)
- Don't replace the square with a circle, checkmark, or period glyph
- Don't put the square anywhere but after the final "a" at baseline
- Don't add a container, badge, or gradient behind the mark

## Files in this folder
- verata-logo.svg — light-background lockup (text as font; convert to outlines for print)
- verata-logo-dark.svg — dark-background lockup
- verata-favicon.svg — favicon/avatar monogram
Note: SVGs reference Geist Mono by name; they render correctly wherever the font is available (or after converting text to paths in Figma/Illustrator). For web use, prefer the HTML/CSS snippet.
