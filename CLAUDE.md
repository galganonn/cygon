# Cygon — Claude Instructions

## What this project is

**Cygon** is a B2B SaaS product for physical security and IoT device management in multi-site enterprise environments (hotels, campuses, etc.). This repo contains high-fidelity interactive prototypes built in vanilla HTML/CSS/JS — no frameworks, no build tools.

The site is published at **`galganonn.github.io/cygon/`** via GitHub Pages.

## Stack

- Vanilla HTML/CSS/JS
- No npm, webpack, bundlers, or anything similar
- Fonts via Google Fonts (CDN, inlined in `<head>`)
- No external JS libraries

## File structure

```
/Cygon/
├── work/
│   ├── cygon-overview.html   ← Device Inventory Overview screen
│   └── cygon-review.html     ← Review Devices screen
├── uploads/                  ← Images and assets
│   ├── ellipse-glow.png      ← Background glow effect
│   ├── logo-lg.png           ← LG brand logo
│   └── logo-samsung.png      ← Samsung brand logo
└── CLAUDE.md                 ← This file
```

## Fonts in use

| Font | Usage | How it loads |
|------|-------|-------------|
| **Figtree** | Primary UI — body, labels, nav | Google Fonts |
| **Poppins** | Page titles, section headings | Google Fonts |
| **JetBrains Mono** | MAC addresses, technical identifiers | Google Fonts |
| **Crimson Pro** | Decorative / editorial text (overview only) | Google Fonts |
| **Plus Jakarta Sans** | Secondary UI text (overview only) | Google Fonts |

## Color system

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#f6f7fb` | App shell, sidebar |
| Surface | `#ffffff` | Cards, content panel |
| Text primary | `#323338` | Headings, body |
| Text secondary | `#676879` | Labels, meta |
| Text tertiary | `#9699a2` | Timestamps, hints |
| Primary blue | `#0073EA` | Active states, CTAs, brand |
| Border | `#d0d4e4` | Card borders, dividers |
| Border light | `#e7e9ef` | Panel edges |
| Green | `#00C875` | Active / approved / healthy |
| Red | `#df2f4a` | Violations, errors |

## Product layout (both screens)

- **Top bar** — 48px, brand mark + icons + avatar (`RS` initials, `#0073EA`)
- **Sidebar** — 56px wide, icon + label nav items. Active item: icon area has `#cce4ff` bg
- **Content panel** — white, `border-top-left-radius: 16px`, subtle glow image behind content
- **Nav items**: Overview, Locations, Alerts, Security, Devices, Networks, Zones, Mgmt, Settings

## Screen inventory

### `cygon-overview.html` — Device Inventory Overview
- KPI summary cards (violations, pending, identified, sites)
- AI "Piper" ask-bar with suggestion chips
- Pulse dot animation on active alerts

### `cygon-review.html` — Review Devices
- KPI cards row
- Violation alert banner (red left border)
- Page-level tabs: All / New / Registered
- Location segmented control: All / Tel Aviv / Jerusalem / Eilat
- Device rows: `border-left: 3px solid #00C875` for approved, red for violations
- Expandable rows with manufacturer logos
- Bottom action bar: "Skip for now" / "Approve all 19"

## Code conventions

- All CSS lives in a `<style>` block in `<head>`
- CSS classes used throughout (not inline `style=""` attributes)
- Section comments in CSS: `/* ── SECTION NAME ── */`
- All JS in a `<script>` block before `</body>`, in `DOMContentLoaded`
- Animations via `@keyframes` (e.g. `pulse-ring`, `device-row-out`)
- Transitions: `140ms ease` standard, `160ms ease` for input focus

## Git

- Main branch: `main`
- Remote: `cygon` → `https://github.com/galganonn/cygon.git`
- This repo contains ONLY Cygon files — portfolio content lives in a separate repo
