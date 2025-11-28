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
- HTML5 + CSS3 only (no JS).
- Custom fonts via `@font-face` (WOFF2).

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

## Local Preview
You can open `index.html` directly in the browser, or use a static server (recommended to avoid font/CORS quirks):

- PowerShell + Python (built‑in on many systems):
```powershell
python -m http.server 8080; Start-Process http://localhost:8080
```

- Node (http-server):
```powershell
npm install -g http-server; http-server -p 8080; Start-Process http://localhost:8080
```

- VS Code Live Server:
1) Install the “Live Server” extension.
2) Right‑click `index.html` → “Open with Live Server”.

## Responsive Behavior
- ≤ 1280px: KPI cards switch to a 2‑column grid; Projects/Events become fluid width; decorative Events bar hides automatically.
- ≤ 900px: Table hides Customer and Sent Date columns for readability.
- ≤ 600px: Single‑column KPI grid; smaller button; table shows Project + Amount.
- ≤ 480px: Table rows render as stacked “cards” with inline labels (Project, Customer, Sent Date, Amount, Status).

## Design Tokens (excerpt)
Defined in `:root` of `styles.css` for easy theming:
- `--sidebar-width`, `--color-active-accent` (`#1CD2AD`), `--color-border`, `--hero-bg`, etc.

## GitHub: Initialize, Push, and Publish (Pages)
1) Create a new GitHub repository (empty, no templates).
2) In PowerShell from the `task` folder:
```powershell
git init; git add .; git commit -m "feat: initial dashboard";
git branch -M main; git remote add origin https://github.com/<you>/<repo>.git;
git push -u origin main
```
3) Enable GitHub Pages:
- Repo Settings → Pages → Source: `Deploy from a branch`
- Branch: `main` / Folder: `/ (root)` → Save.
- Your site will be available at: `https://<you>.github.io/<repo>/`.

## Customization
- Images: Replace icons/avatars in `images/`. Keep file names or update the `src` in HTML.
- Colors/spacing: Adjust CSS variables in `styles.css`.
- Fonts: Point `@font-face` to your own font files if file names differ.

## Accessibility Notes
- Images include `alt` text; interactive controls are keyboard focusable.
- Color contrast aligns with the original design; adjust variables if you need higher contrast.

## Fonts & Licensing
Gilroy is a commercial typeface. This project references WOFF2 files placed in the local `Gilroy/` folder. Ensure you have a valid license to use and distribute these fonts, or substitute with licensed alternatives. The UI will fall back to system fonts if Gilroy is unavailable.

## Known Limitations
- Static data (no backend). Update table rows / events directly in `index.html`.
- The decorative vertical bar in Events is hidden automatically on smaller screens to avoid overlap.

## Credits
- Design: Provided Figma frames/specs.
- Implementation: Static HTML/CSS authored for a pixel‑faithful replica.
