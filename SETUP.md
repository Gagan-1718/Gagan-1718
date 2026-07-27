# ⚙ SETUP & CUSTOMISATION

Everything you need to make this profile yours. Nothing here shows on the profile —
GitHub only renders `README.md`.

---

## 📂 Folder structure

```text
Gagan-1718/                     ← must be named exactly like your username
│
├── README.md                   ← the profile itself (the only rendered file)
├── SETUP.md                    ← this guide
│
├── assets/
│   ├── banner.svg              ← hero: name, tagline, HUD, city, CV feed, neural net
│   ├── divider.svg             ← animated neon divider (reused between sections)
│   ├── dossier.svg             ← player dossier / system status cards
│   ├── inventory.svg           ← tech inventory cards
│   ├── skill-tree.svg          ← radial skill tree with energy pulses
│   └── footer.svg              ← end-of-transmission strip
│
└── .github/
    └── workflows/
        └── snake.yml           ← generates the contribution snake (optional)
```

Optional slots if you extend the design later: `assets/icons/` for custom glyphs,
`assets/projects/` for per-project cover art.

---

## ✅ Replace-this checklist

Search the README for `⚙ REPLACE` — every spot is commented. In order:

| # | Where | What to change |
| :--- | :--- | :--- |
| 1 | `08 // COMMS UPLINK` | LinkedIn, portfolio, email, X handle |
| 2 | `06 // FEATURED OPERATIONS` | 4 project names, one-line briefs, tech chips, code + demo links |
| 3 | `05 // ACTIVE QUESTS` | your real objectives and progress bars |
| 4 | `01 // PLAYER DOSSIER` (details table) | city / region |
| 5 | `assets/dossier.svg` | the `LOCATION` card — search the file for `⚙ EDIT` |

Everything else (username, stats, streak, languages, activity graph) is already
wired to `Gagan-1718`.

---

## 🎨 Palette

Keep these exact values so every panel stays cohesive.

| Token | Hex | Used for |
| :--- | :--- | :--- |
| Background | `#09090B` | page + all SVG backgrounds |
| Panel | `#0B0F16` | glass cards |
| Primary — neon cyan | `#22D3EE` / `#67E8F9` | borders, headings, primary glow |
| Electric blue | `#3B82F6` / `#7CB0FF` | Core CS branch |
| Secondary — purple | `#A855F7` / `#C99BFF` | AI/ML branch, accents |
| Accent — neon green | `#3BFFA1` / `#7CFFC4` | status "online", frameworks |
| Small accent — hot pink | `#FF2E88` / `#FF6FAE` | data stores, sparingly |
| Text | `#F4F7FB` → `#C9D6E4` → `#8B95A7` → `#5D6B7E` | primary → muted |

---

## 🐍 Contribution snake (optional)

1. Push this repo.
2. Go to **Actions** → enable workflows if prompted.
3. Run **Generate Snake** once manually; after that it runs every 12 hours.

Until it runs once, the snake image at the end of `07 // TELEMETRY` will not load —
either run it or delete that block from the README.

---

## ✏️ Editing the SVGs

They are hand-written and commented — open any of them in a text editor.

- **Change the tagline:** `assets/banner.svg`, search for `Software that sees`.
- **Change a skill or its meter:** `assets/skill-tree.svg` — each chip is a `<rect>`
  label plus a two-pixel meter bar; shrink the second bar's `width` to lower the level.
- **Add an inventory item:** `assets/inventory.svg` — copy a `<text>` row inside a card
  and add `+32` to its `y`. Keep item text under ~18 characters so it stays inside the card.
- **Animation speed:** every `dur="Xs"` is independent; raise the number to calm it down.

Preview locally by opening the `.svg` file in any browser — animations play there
exactly as they do on GitHub.

---

## 📱 Notes that matter

- **Mobile:** every image is `width="100%"`, so panels scale down. Dense SVGs get small on
  a phone — that is why the dossier and inventory each ship a `<details>` text version below
  them. Keep those in sync when you edit.
- **Dark theme:** backgrounds are baked into the SVGs, so panels look identical in GitHub's
  light and dark themes. Only the code blocks and tables follow the viewer's theme.
- **Animations:** SMIL (`<animate>`, `<animateMotion>`) is used, not CSS/JS — that is the
  subset GitHub's image proxy actually plays.
- **Caching:** GitHub caches images aggressively. After editing an SVG, hard-refresh
  (`Cmd/Ctrl + Shift + R`) or wait a few minutes before judging the result.
