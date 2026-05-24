# AGENTS.md

Guidance for AI coding agents working in this repository.

## Project overview

This is the public website for **Epsilon Quantitative ApS**, an automated/algorithmic
energy trading company based in Aarhus, Denmark. The site is a single static page
served via **GitHub Pages** at the custom domain `epsilonquant.com` (configured in
`CNAME`).

Everything committed here is published publicly and automatically by GitHub Pages.
**Do not add anything that is not intended for public consumption** (no secrets,
credentials, internal documents, or private data).

## Repository layout

- `index.html` — the entire site. A single self-contained page with all CSS inlined
  in a `<style>` block in the `<head>`. There is no build step, framework, or
  bundler.
- `CNAME` — custom domain for GitHub Pages (`epsilonquant.com`). Do not remove or
  edit unless intentionally changing the domain.
- `epsilon-quantitative-logo*.jpg` / `.svg` — brand logo assets. `index.html`
  currently references `epsilon-quantitative-logo.jpg`.
- `favicon.ico` — site favicon.
- `README.md` — short note explaining the repo is published publicly.

## Conventions

- **No build tooling.** Edit `index.html` directly; changes are deployed on push to
  the default branch. To preview, open `index.html` in a browser — no server needed.
- **Styling lives inline** in the `<style>` block. Use the existing CSS custom
  properties under `:root` (the `--space-*` spacing scale and `--bg-color` /
  `--text-*` color tokens) rather than introducing ad-hoc values.
- Keep the page **self-contained and dependency-free**; avoid adding external
  scripts, fonts, or CSS frameworks.
- Preserve the dark theme and brand colors (background derives from the logo,
  `rgb(57, 57, 57)`).
- Markup is semantic and accessible (e.g. `<address>`, `<dl>` contact grid, SVG icons
  marked `aria-hidden`). Keep accessibility attributes intact when editing.
- Company contact details (address, phone, email, VAT ID, LinkedIn) appear in the
  contact block — keep them accurate and consistent.

## Validation

There are no automated tests. Before committing changes to `index.html`:

- Open the page in a browser and confirm layout renders correctly.
- Check the responsive layout at mobile widths (there is a `@media (max-width: 480px)`
  breakpoint).
- Verify all links (`tel:`, `mailto:`, LinkedIn, VAT lookup) still work.
