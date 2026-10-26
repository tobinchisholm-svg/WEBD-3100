# FuelFare — Colour System V1

WEBD 3100 — Workshop 03A | Tobin Chisholm | Fall 2026

FuelFare is a trip cost calculator that shows drivers what a trip from point A to point B will cost in gas, based on their vehicle and local gas prices. This folder contains the project's colour system: design tokens, light and dark themes, and a responsive demo page.

## Base colour

| Format | Value |
|---|---|
| HEX | `#D72638` |
| RGB | `rgb(215, 38, 56)` |
| HSL | approx. `hsl(354, 70%, 50%)` |

**Inspiration:** car dashboards at night: a black instrument panel with red gauge needles and warning lights. The goal is a sleek, bold, modern look that stays clear and easy to read.

**Supporting colours:** near-black `#141414` (secondary), light red `#FF4D5E` (accent), steel grey `#6B7280` (neutral), off-white `#F5F5F5` (light background).

## Generation method

The 11-step ramp (50–950) was generated with **RGB Mix**, which blends each RGB channel toward white for lighter steps and toward black for darker steps. Step 500 is the base colour. OKLCH was also generated and compared; RGB Mix was chosen as the provisional ramp because its values are easy to verify by hand and match the exported tokens. The darker steps may be revisited with OKLCH for richer dark-theme reds.

## Theme design

Components use **semantic tokens** (`--color-background`, `--color-surface`, `--color-text`, `--color-primary`, `--color-on-primary`), so the same HTML and component CSS work in both themes.

- **Light theme:** off-white page, white cards, near-black text, red buttons with white text.
- **Dark theme:** near-black page and cards, light text, red buttons with white text.

### Contrast results (WCAG 2.x AA, normal text needs 4.5:1)

| Theme and component | Text | Background | Ratio | Result |
|---|---|---|---|---|
| Light — body text | `#141414` | `#FFFFFF` | 18.42:1 | Pass |
| Light — primary button | `#FFFFFF` | `#D72638` | 4.97:1 | Pass |
| Dark — body text | `#F5F5F5` | `#141414` | 16.90:1 | Pass |
| Dark — primary button | `#FFFFFF` | `#D72638` | 4.97:1 | Pass |

**Revision:** the exported dark theme originally used a navy background and a pink button with navy text. It was changed to near-black surfaces and the base red with white text to match the black-and-red design, and retested (passes AA).

Important information is never shown by colour alone. Buttons and statuses always include text labels.

## How to preview

1. Open this folder in VS Code.
2. Right-click `index.html` and choose **Open with Live Server**.
3. Dark theme is on by default (`data-theme="dark"` on the `<html>` tag). Remove that attribute and save to see the light theme.
4. Use the browser's responsive mode to test at 375 px, 768 px, and 1280 px.

## Files

```
├── index.html
├── css/
│   ├── tokens.css       # foundation ramps, semantic tokens, light/dark themes
│   ├── base.css         # global styles and fluid page container
│   └── components.css   # card, card grid, and button components
└── README.md
```
