# TrackInc Dashboard (Static HTML/CSS)

A pixel‑faithful implementation of the TrackInc dashboard from Figma using semantic HTML and modern, responsive CSS. It includes the left sidebar, hero header, KPI cards, the Current Projects table, and the Events panel — matching the specified sizes, positions, and typography.

## Features
- Sidebar: fixed on desktop with active state and icons.
- Hero Header: greeting, search, notifications, and avatar; "Finance Overview" title.
- KPI Cards: 4 metric cards with exact sizes, borders, and bottom‑right icons.
- Current Projects: 1157×520 panel with 16px radius, light shadow, header and “Create” button, grid table with badges.
- Events Panel: 453×332 card with title, avatar list, small blue chips, and a decorative vertical bar (desktop only).
- Typography: Gilroy Regular/SemiBold/SemiBoldItalic across UI; Inter/Plus Jakarta Sans used where specified.
- Responsive: Fluid layout for tablets/phones; table progressively simplifies to a stacked card layout on small screens.

## Tech Stack
- HTML5 + CSS3 only.
- Custom fonts via `@font-face`.

## Project Structure
```
├─ index.html
├─ styles.css
├─ README.md
├─ images/
│  ├─ track.png, Inc.png, ...
│  ├─ events human 1.png … events human 4.png
└─ Gilroy/
   ├─ Gilroy-Regular.woff2
   ├─ Gilroy-SemiBold.woff2 (and fallback casing)
   └─ Gilroy-SemiBoldItalic.woff2 (and fallback casing)
```

