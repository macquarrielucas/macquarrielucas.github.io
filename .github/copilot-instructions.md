# Copilot Instructions for Hugo_site_2

## Project Overview
This is a Hugo static site using the `hello-friend-ng` theme. Content is managed via Markdown and TOML files, with custom layouts and assets. The site is deployed to GitHub Pages using a CI workflow.

## Key Directories & Files
- `hugo.toml`: Main site configuration (base URL, theme, params, menus, taxonomies)
- `content/`: Site content (Markdown)
- `static/`: Public static assets (images, CSS, downloads)
- `layouts/`: Custom HTML templates and partials
- `themes/hello-friend-ng/`: Theme source, including its own config and docs
- `.github/workflows/hugo.yaml`: GitHub Actions workflow for build/deploy

## Build & Deployment
- **Local build:** Run `hugo` in the project root to generate the site in `public/`.
- **Production deploy:** Pushing to `main` triggers GitHub Actions (`.github/workflows/hugo.yaml`) to build and deploy to GitHub Pages.
- **Theme updates:** Theme is managed as a submodule; update via `git submodule update --remote`.

## Content & Customization
- **Content:** Add/edit Markdown files in `content/`. Front matter supports custom fields (e.g., `audio` for posts with audio).
- **Menus:** Defined in `hugo.toml` under `[[menu.main]]`.
- **Images:** Place in `static/images/` and reference as `/images/...`.
- **Custom CSS:** Add to `static/css/custom.css`.
- **Portrait:** Set via `[params.portrait]` in `hugo.toml`.

## Theme-Specific Features
- **Shortcodes:** Use Hugo and theme-provided shortcodes (see theme README for examples).
- **Code highlighting:** Use triple backticks in Markdown; PrismJS is used for syntax highlighting.
- **Social icons:** Configure in `hugo.toml` under `[[params.social]]`.
- **Multilingual:** Enable/disable global language menu via `enableGlobalLanguageMenu` in `hugo.toml`.

## Conventions & Patterns
- **No Node.js required for theme edits.**
- **Taxonomies:** Defined in `hugo.toml` (`tags`, `categories`, `series`).
- **Caching:** Images cache configured in `[caches]` section of `hugo.toml`.
- **Front matter:** YAML/TOML front matter in Markdown files supports custom fields (e.g., `audio`).

## External Integrations
- **GitHub Pages:** Automated deploy via workflow.
- **Theme:** [hello-friend-ng](https://github.com/rhazdon/hugo-theme-hello-friend-ng) (MIT License)

## Example Workflow
1. Edit content in `content/` or assets in `static/`.
2. Run `hugo` to preview locally.
3. Commit and push changes to `main`.
4. GitHub Actions builds and deploys to Pages.

## References
- Theme docs: `themes/hello-friend-ng/README.md`
- Hugo docs: https://gohugo.io/

---
If any section is unclear or missing, please provide feedback for further refinement.
