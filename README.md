# Runway ✈️

**Never sprint to the gate again.**

Runway is a single-page tool for planning your trip to the airport. Enter your
flight's departure time and it works backwards through your morning — wake-up,
getting ready, the ride or drive over, security, boarding — to tell you exactly
when to set your alarm.

No build step, no dependencies, no backend. It's one static HTML file.

## Features

- **Works backwards from your flight time.** Your departure time is treated as
  a fixed fact — editing any earlier step (like "wake up") absorbs the change
  into your airport cushion instead of silently moving your flight.
- **Pin any step** to anchor the whole plan around it instead, if you'd rather
  fix your wake-up time and see everything shift around that.
- **Four transport modes** (Drive, Rideshare, Transit, Drop-off) that reshape
  the timeline — swapping in parking/shuttle steps, ride-wait steps, or station
  walks as appropriate.
- **A cushion verdict** ("Roomy" / "Snug" / "Tight") based on how much slack
  you have once you're through security, with an international-flight toggle
  that raises the recommended buffer.
- **Copy your plan as text**, **copy a shareable link** that reproduces your
  exact plan when opened, or **print** a clean, ink-friendly version.
- Full light/dark theme support, keyboard accessible, works down to narrow
  mobile widths.

## Running it

There's nothing to install. Just open `index.html` in a browser, or serve the
folder with any static file server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploying

Because it's a single static file, this repo works as-is with:

- **GitHub Pages** — push to a repo, enable Pages in Settings → Pages, point
  it at the branch root (`index.html` is already named correctly for that).
- **Netlify / Vercel / Cloudflare Pages** — drag-and-drop the folder or connect
  the repo; no build command needed.
- Any plain web host — just upload `index.html`.

## Project structure

```
.
├── index.html   # the entire app — markup, styles, and script in one file
├── README.md
└── LICENSE
```

## License

MIT — see [LICENSE](LICENSE).
