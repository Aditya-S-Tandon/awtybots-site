# AwtyBots · FRC Team 5829 — Website

Static site for **FIRST Robotics Competition Team 5829**, the AwtyBots, at the
Awty International School in Houston, TX. Hosted on GitHub Pages.

## Architecture

The **homepage (`index.html`)** uses a custom, dependency-free design system:

| File | Purpose |
|------|---------|
| `index.html` | Redesigned homepage markup |
| `assets/css/site.css` | Design system — colors, type, components, animations |
| `assets/js/site.js` | Interactions — scroll reveals, count-up stats, live countdown, card tilt, auto-path draw, flag marquee |
| `assets/images/web/` | Web-optimized photos used by the homepage |

Plain HTML/CSS/JS — no build step, no framework. Fonts come from Google Fonts
(Saira, Inter, JetBrains Mono). Edit content in `index.html`, the look in
`assets/css/site.css`, behavior in `assets/js/site.js`.

> The **inner pages** (`robots.html`, `events.html`, `recaps.html`, `outreach.html`)
> still use the original Bootstrap template and will be migrated to the new design next.

## Run it locally

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploy on GitHub Pages

### Replace the existing live site (recommended)
Push these files to the existing `awtybots.github.io` repo's default branch. The
`CNAME` (`www.awtybots5829.org`) stays as-is and the custom domain keeps working.

### Or publish as a brand-new repo
1. Create a new empty repo on GitHub (e.g. `awtybots-site`).
2. Add the remote and push:
   ```bash
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
3. In **Settings -> Pages**, set Source = `main` branch, root.
4. **Custom domain note:** `www.awtybots5829.org` can only point to ONE repo. If you're
   keeping the old repo live, delete the `CNAME` file here and use the
   `https://<you>.github.io/<repo>/` URL instead.

## Credits
(c) 2015-2026 The AwtyBots Team, Awty International School. Content CC BY 4.0.
