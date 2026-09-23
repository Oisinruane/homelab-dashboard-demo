# Homelab Dashboard (Public Demo)

A static, mock-data build of my private homelab dashboard — a single page that pulls together
status widgets for everything running on my home server (Proxmox, Pi-hole, the *arr stack,
qBittorrent, Jellyfin, and a few other bits) into one view.

This repo is a one-time export of that dashboard's demo/mock-data mode. It has no API routes,
no server, and no connection to my actual home network — every widget shows fake data, and
nothing you click is saved anywhere. It exists purely so the design and layout can be shown
publicly (e.g. embedded on my [personal website](https://github.com/Oisinruane/Personal_website))
without exposing the real, private dashboard.

## Quick start

It's a plain static export — no build step needed to view it.

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Design language

- **Framework:** Next.js 14, exported as a static site
- **Styling:** Tailwind CSS, dark theme, widget-grid layout
- **Charts:** Recharts
- **Layout:** a responsive grid of self-contained widget cards (usage graphs, DNS stats,
  media, calendar, infrastructure status, project tracking), with a bottom tab bar
  (Home / IoT / Infrastructure / Media / Projects) grouping widgets by category

See `docs/overview.md` for more on what's in this repo.

## License

Demo/portfolio use only — see the personal website above for how this fits into the wider
project.
