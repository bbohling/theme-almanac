# Almanac — a micro.blog theme

A Swiss-style, photo-first theme where every snippet is led by its date: a huge condensed day number, the month and weekday, then the photo. Black, white and one accent color.

What it includes:

- **Home:** a month-by-month strip at the top, with one dot for each post (each month links to the archive), then a dated feed with a big outlined year mark wherever the year changes. Photo posts show the first photo large, with up to four more as thumbnails. Text-only posts are set large, like a pull quote.
- **Single post:** a giant date header, the full post, category pills, micro.blog conversation and links to the posts before and after.
- **Archive (`/archive/`):** a calendar. Each year has a grid of months, and each post is a small day tile (a photo thumbnail when the post has one).
- **Photos (`/photos/`):** a square grid with date labels.
- **Categories and pages:** the same type system.
- **Dark mode:** follows the system setting automatically.

## Install (custom theme from GitHub)

1. Create a **public** GitHub repo and push the contents of this folder to it (`plugin.json`, `config.json`, `layouts/` and `static/` at the top level).
2. On micro.blog, go to **Posts → Design → Edit Custom Themes → New Theme**.
3. Pick **Blank** as the base and paste the repo URL to clone it.
4. Go to **Posts → Design**, select the new theme and save.

To change a template later, edit it in micro.blog's theme editor or push to the repo and re-clone.

## Settings

Edit the `params` block at the bottom of `config.json`:

| Param | Default | What it does |
|---|---|---|
| `almanac_tagline` | `Snippets, by the day` | The line under your name |
| `almanac_accent` | `#D7261E` | The single accent color (dots, weekdays, counts) |
| `almanac_show_strip` | `true` | Shows or hides the month strip on the home page |
| `almanac_strip_months` | `18` | How many months the strip covers (3–36) |
| `almanac_home_count` | `30` | Posts on the home page when micro.blog's home pagination is off |
| `almanac_show_time` | `false` | Adds the time of day next to each date in the feed |

The theme also respects micro.blog's own `paginate_home` and `include_conversation` settings.

You can override any style from **Design → Edit CSS**: `custom.css` loads after `almanac.css`. All the colors are CSS variables on `:root` (`--bg`, `--ink`, `--muted`, `--panel`, `--accent`).

## Notes

- Fonts: Archivo (variable width) from Google Fonts. The big numerals use its condensed width axis.
- Your nav comes from your micro.blog pages and menu, as before. Pages with a redirect URL are respected.
- `plugin.json` is included so the same repo can later be published as a micro.blog plug-in with a settings screen. For a plug-in, trim `config.json` down to just the `params` block.
