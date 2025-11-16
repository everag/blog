# Ev’s Blog (Hugo + Bear)

This repository contains the source for a Hugo-powered blog that uses the “Hugo Bear Blog” theme.

- Static site generator: Hugo
- Theme: hugo-bearblog (by Jan Raasch)
- Site source: /
- Output: typically published to the docs/ folder for GitHub Pages

## Local development

From the repository root:

    hugo server -D

Then open the local URL printed by Hugo (usually http://localhost:1313).

Requirements:
- Hugo (extended) — see https://gohugo.io/getting-started/installing/
- Git (to pull the theme submodule, if applicable)

## Building the site

To build the static site locally:

    hugo --minify

If the site is configured with `publishDir = "docs"` in `hugo.toml`, the built site will appear under `docs/` at the repository root, suitable for GitHub Pages.

If you prefer a one-off build to a specific directory:

    hugo --minify --destination ../docs

Optional (recommended for GitHub Pages):
- Add an empty `.nojekyll` file so Pages serves files as-is.
- If you use a custom domain, ensure a `CNAME` file is included in the output.

## Deploying to GitHub Pages (without CI)

The simplest approach is to serve from the default branch’s `/docs` folder:

1. Build locally into `docs/` as shown above.
2. Commit and push `docs/` to your default branch.
3. In your repository settings:
   - Pages → Build and deployment → Source: “Deploy from a branch”
   - Branch: `main` (or your default), Folder: `/docs`

If you use a custom domain, configure DNS and include a `CNAME` file in `docs/`.

## Theme

This site uses the third-party theme:

- hugo-bearblog — https://github.com/janraasch/hugo-bearblog
  The theme’s license is included under [themes/hugo-bearblog/LICENSE](themes/hugo-bearblog/LICENSE) and applies to the theme files.

## Licensing

- Software (site configuration, templates, styles, and any custom code you authored in this repository): MIT License. See the [LICENSE](LICENSE) file at the repository root.
- Content (all original posts, pages, and media): All Rights Reserved. See [CONTENT-LICENSE](CONTENT-LICENSE) for terms.

Note on generated output:
- The built site (e.g., in `docs/`) contains both software and content. The text and media remain All Rights Reserved; the design and templating remain under their respective software licenses.

---
Questions or requests for content reuse? Please open an issue or contact the repository owner.
