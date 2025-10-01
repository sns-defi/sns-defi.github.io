# DeFi & Crypto Conference @ Scuola Normale Superiore (Pisa)

A lightweight, Bootstrap-styled Jekyll site ready for GitHub Pages. Pages are defined in `_data/navigation.yml`.

## Quick start

1. Create a new GitHub repository (public is fine).
2. Upload the contents of this folder to the repository root (or unzip and push via Git).
3. In **Settings → Pages**, choose **Deploy from branch**, then select the `main` branch and the `/ (root)` folder. Save.
4. Wait for Pages to build, then visit your site URL shown in the Pages section.

> If this is a **project site** (URL like `https://username.github.io/repo`), set `baseurl: "/repo"` in `_config.yml`.

## Customize

- Site title/description: edit `_config.yml`.
- Menu items: edit `_data/navigation.yml`.
- Add speakers by editing `_data/speakers.yml`.
- Theme tweaks: edit `assets/css/custom.css` (uses Bootstrap 5).

## Content pages

All pages are Markdown with YAML front matter and use the shared layout:
- `index.md` — Homepage
- `program.md` — Program
- `registration.md` — Registration
- `submission.md` — Paper Submission
- `venue.md` — Venue
- `committee.md` — Committee
- `speakers.md` — Invited Speakers

## Development (optional)

You can run Jekyll locally if you want:

```bash
gem install bundler jekyll
bundle init
bundle add jekyll jekyll-seo-tag
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000

## License

MIT — feel free to adapt.
