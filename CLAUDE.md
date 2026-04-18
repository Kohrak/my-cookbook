# my-cookbook

## Project

Weight-loss cookbook published as a static site via GitHub Pages from the `main` branch of this repo.

The source recipes live in `recipes.md` each with calorie count and macros (protein, carbs, fat). All recipes are ~600-730 kcal, high protein. Recipes 18-20 have less detail than the rest (no gram weights).

The site should be static HTML/CSS, deployable from the repo root or a `/docs` folder.

All written content must use British English spelling and conventions.

---

## Visual Style

A handcrafted, archival aesthetic — warm paper tones, forest greens, and inky browns. Typeset with a mix of serif, monospace-serif, and handwriting fonts to evoke an old document or field guide.

### Google Fonts
Special Elite | Lora (400, 400i, 600, 600i) | Caveat (400, 600)

### CSS Variables
```css
--paper:       #f2e8d0;
--paper-dark:  #e5d9bc;
--paper-mid:   #ecdfc5;
--ink:         #2a1f0e;
--ink-mid:     #6b5a3e;
--ink-light:   #9a8a6a;
--green:       #4a7a4a;
--green-mid:   #6a9e6a;
--green-light: #9ec49e;
--green-pale:  #d4e8d4;
--amber:       #b8722a;
--amber-pale:  #f0d8a8;
--stamp-red:   #8b2020;
--stamp-blue:  #1a3a6a;
--border:      #c8b890;
```

### Base
- Body background: dark forest gradient (`#2d3a28 → #3a4a30 → #1e2e1a`)
- Document container: max-width 920px, bg `--paper`, border `1px solid --border`
- Box shadow: `0 0 0 1px border, 4px 4px 0 #1a2614, 8px 8px 0 #141e10, 0 20px 60px rgba(0,0,0,.5)`
- Base font: 15px Lora, line-height 1.7, color `--ink`

### Typography Rules
- Headings/labels: Special Elite, uppercase, letter-spacing 2-3px
- Handwritten annotations: Caveat, italic
- Section titles: Special Elite 0.68rem uppercase `--green`, letter-spacing 3px, border-bottom `1px solid --green-light`, `::before` `"❧"` in `--green-mid`

### Key Components
- **Archive band (top bar):** bg `--ink`, text `--paper`, Special Elite 0.7rem uppercase
- **Tags:** bg `--green-pale`, color `--green`, border `--green-light`, Special Elite 0.7rem, border-radius 2px. Alt variant: `--amber-pale` / `--amber`
- **Chronicle box:** bg `--paper-dark`, border `1px solid --border`, border-left `3px solid --green-mid`
- **Record items:** dashed top border, bullet `"✦"` pseudo-element in `--amber`
- **Stamps:** Special Elite uppercase, 2px border, slight rotation, colors `--stamp-red` or `--stamp-blue`
- **Sidebar:** bg `--paper-mid`, titles in `--amber` Special Elite 0.62rem uppercase
- **Vine divider:** flex row, 1px gradient line (`--green-light → --border → --green-light`), small SVG in `--green-mid`
- **Handwritten notes:** Caveat, color `--green`, italic, opacity ~0.75
- **Footer:** bg `--paper-dark`, border-top `2px solid --border`

### Layout
- 2-column grid: `1fr 255px` (main + sidebar)
- Responsive: single column below 700px
- Falling leaves animation: fixed, pointer-events none, z-index 0
