# DigiFarm — UI Guidelines

A single-page, static HTML reference for DigiFarm's design system — design tokens, components, patterns, and full-page block examples used across client-facing demos and internal tools.

**[View live](#)** — replace with your GitHub Pages URL once deployed (see below).

## What's inside

`index.html` is the whole thing — one self-contained file, no build step. It covers:

**Foundation**
- Logo — brand mark on its dark tile, reference sizes
- Partners — 20+ partner/integration logos, light and dark variants, light-tile logos listed first
- Colors, Typography, Spacing & Radius
- Flags — 250 countries via the `country-flag-icons` CDN, full-width grid, click to copy

**Components**
- Buttons — variants, sizes, states, underlined links
- Buttons with icons — leading/trailing icon slots, icon-only buttons
- Segmented Control — default, small, with icons, and disabled states
- Inputs & Forms — text states (including error hint pattern), Input with Label (label-top/input-bottom, three states), icon inputs, slider, select
- Radio — label/description/status field integration, disabled state
- Checkbox — single on/off toggle, indeterminate state, disabled state
- Dropdown / Dropdown items — trigger states and the option-list panel
- Badges & Tags — default and small sizes, five statuses (active, review, offline, in progress, pending)
- Cards & Surfaces, Selectable Cards
- Avatar — sizes, no-color/neutral variant, status indicators, avatar groups, hover-to-reveal name, User Card example
- Alerts — five semantic variants (neutral, info, warning, error, success), plus icon-less variants
- Banner — status header with optional icon, dismiss, action button, and collapsible content area
- Calendar — single date, date range, and two-month range pickers
- Table — two-line field cells, striped rows, hover highlight, anchored row-actions dropdown, sortable Area column
- Tooltip — top/bottom placement, icon/button/text/badge triggers
- Draggable Cards — live vertical reordering
- Loaders — five CSS-only spinners in brand colors

**Patterns**
- Map UI Elements — overlay panels, layer controls, coordinate display
- CSS Variables — the full `:root` token block, copy-paste ready

**Blocks** (full composed examples)
- Login / Registration — access-code + email sign-in flow with a request-account modal
- Crop Classification
- Productivity Zones
- Time Series
- Field Sustainability Index
- Illustrations — spot illustrations for empty states, onboarding, marketing
- Icon Library — all 2,267 Remix Icon icons, searchable, grouped into 17 categories, click to copy

A Changelog card near the top tracks version history in-page.

## Tech / dependencies

Everything loads from CDNs at runtime — there's nothing to install:

- **Fonts** — Inter & IBM Plex Mono via Google Fonts
- **Flags** — [`country-flag-icons`](https://www.npmjs.com/package/country-flag-icons) via jsDelivr
- **Icons** — [Remix Icon](https://remixicon.com) webfont via jsDelivr (Icon Library block, Table row actions)
- **Partner logos / favicon** — hotlinked images (swap for local assets whenever convenient)

No React, no bundler, no `node_modules`. Open `index.html` directly in a browser and it works.

## Local preview

```bash
# any static server works, e.g.
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just double-click `index.html` — it renders standalone.

## Deploying with GitHub Pages

1. Push this repo (with `index.html` at the root) to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, pick your default branch and the `/ (root)` folder.
4. Save — GitHub will publish at `https://<username>.github.io/<repo-name>/`.

The in-page **Download HTML** button (top of the sidebar) also lets anyone export a standalone copy of the current page straight from the browser.

## Updating

The whole file is hand-authored HTML/CSS/JS organized by section — search for the relevant `<section id="...">` block to edit. The sidebar nav links match section `id`s 1:1, so renaming a section means updating both.

When you make a meaningful change, add an entry to the Changelog card at the top of `index.html` (`id="changelog"`) so the version history stays accurate.
