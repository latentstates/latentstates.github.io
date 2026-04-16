# Site Template

`page.html` is the canonical style template for latentstates.org. Copy it to start any new page.

## Placeholders

Replace these HTML comments with actual content:

| Placeholder | Where | What |
|:--|:--|:--|
| `<!-- TITLE -->` | `<title>` tag | Page title (appears before " — Latent States") |
| `<!-- DESCRIPTION -->` | `<meta>` tag | One-line summary for search engines / link previews |
| `<!-- NAV -->` | Inside `.nav-links` | Navigation links (People, About, etc.) |
| `<!-- CONTENT -->` | Between `</nav>` and `<footer>` | Page body — use `.section` (720px prose), `.section-wide` (1200px layouts), or `.grid-section` (12-col) |

## Identity

Dark, cool-gray palette. Near-black background (`#101012`), desaturated blue-gray accent (`#8090a0`). No warm tones, no color pops. Typography pairs geometric sans-serif headings (Syne 800) with light humanist body text (Space Grotesk 300). The feeling is: scientific restraint at the edge of the unknown.

The home page uses Source Serif 4 for a different register (landing constellation). Inner pages all use the Syne + Space Grotesk system captured here.

## Typography quick reference

| Role | Family | Weight | Usage |
|:--|:--|:--|:--|
| Headings | Syne | 700–800 | `h1`, `h2`, `h3` |
| Body text | Space Grotesk | 300 | `p`, prose, lists |
| Labels / metadata | Space Grotesk | 400–500 | `.meta-line`, `.info-label`, dt elements |
| Nav links | Space Grotesk | 400 | `.nav-links a` |
| Logo | Syne | 700 | `.nav-logo` — always "LS" |

## Palette

| Token | Hex | Role |
|:--|:--|:--|
| `--bg` | `#101012` | Page background |
| `--bg-surface` | `#18181a` | Raised surface (cards, panels) |
| `--border` | `#252528` | Borders, dividers |
| `--text-primary` | `#d8d8dc` | Headings, strong text |
| `--text-secondary` | `#a0a0a8` | Body text |
| `--text-muted` | `#707078` | Labels, captions, metadata |
| `--accent` | `#8090a0` | Links |
| `--accent-alt` | `#a0a8b0` | Link hover |

## Available components

- **`.section`** / **`.section-wide`** — centered containers (720px / 1200px)
- **`.hero`** + **`.hero-image`** — full-width hero below nav
- **`.hero-info`** — title block with optional `.meta-line`
- **`.intro`** — large lead paragraph (20px)
- **`.text-section`** — body text with h2, paragraphs, and em-dash lists
- **`.grid-section`** — 12-column asymmetric layout (`.col-images` left, `.col-text` right)
- **`.image-cluster`** — stacked images with 4px gap
- **`.image-row`** — horizontal image strip (`.image-row--halves`, `--thirds`, `--wide-left`)
- **`.image-caption`** — small muted caption below images
- **`.card-grid`** + **`.card`** — 4-column cards with image, title, description
- **`.metadata-grid`** — key-value pairs (120px label column)
- **`.credits-grid`** — key-value pairs (140px label column)
- **`.divider`** — 48px horizontal rule
- **`.info-section`** — label + text block (links, contact, etc.)
- **`blockquote`** — left-bordered italic pull quote
- **`.project-nav`** — prev/next project links at page bottom

## Page patterns

**Project page**: hero image, hero-info (h1 + meta-line), intro paragraph, text-sections with image clusters, credits-grid, project-nav, footer.

**About/info page**: hero-info (h1 only, no image), text-section with prose, divider, info-sections for links/contact, footer.

## Rules

- All CSS is inline in `<style>`. No external stylesheets, no frameworks.
- Only external dependency: Google Fonts (Syne + Space Grotesk, preconnected).
- Dark palette only. Colors via CSS custom properties in `:root`.
- Two responsive breakpoints: 768px (tablet) and 480px (phone).
- Nav is fixed with backdrop blur. Logo links to `../index.html`.
- Images use `loading="lazy"` except hero.
- Footer is always `Latent States · Lisbon`.
