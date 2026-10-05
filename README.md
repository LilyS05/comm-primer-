# Communication Theory Primer Website

This repository contains a Jekyll-powered GitHub Pages site scaffold for presenting communication theory to non-technical audiences.

## What is included

- Jekyll site configuration for GitHub Pages
- Home page and six structured subpages for your analysis
- Reusable layout with navigation and accessibility-focused semantic/ARIA structure
- Blue color palette stylesheet
- `images/` folder for your media assets
- GitHub Actions workflow that builds and deploys on every push to `main`

## Project structure

- `_config.yml` — core site settings (title, URL, base URL, language)
- `_layouts/default.html` — shared page layout and navigation
- `assets/css/style.scss` — global styles and color variables
- `index.md` — home page
- `transmission-view-limits.md`
- `meaning-and-culture.md`
- `interpretation-and-power.md`
- `interpretation-and-intention.md`
- `what-the-reader-should-do.md`
- `how-i-built-this-site.md`
- `images/` — place images here
- `.github/workflows/pages.yml` — build/deploy workflow

## Writing and updating content

1. Open any `.md` page in the repository root.
2. Keep the YAML front matter at the top of each page unchanged unless you want to rename title/permalink.
3. Replace placeholder text with your own writing.
4. Use Markdown headings, lists, links, and emphasis for structure.
5. Add images from the `images/` folder using paths like:

   ```md
   ![Descriptive alt text]({{ '/images/your-image-name.png' | relative_url }})
   ```

6. Commit and push to `main`; GitHub Actions will rebuild and publish.

## Add a new page

1. Create a new `.md` file in the repository root.
2. Add front matter:

   ```yaml
   ---
   layout: default
   title: "Your Page Title"
   permalink: /your-page-slug/
   ---
   ```

3. Add page content under the front matter.
4. Add a link to the new page in `_layouts/default.html` navigation.

## Customize basic style variables

Edit `assets/css/style.scss` and adjust variables under `:root`:

- `--color-primary-900`, `--color-primary-700`, `--color-primary-600`
- `--color-primary-100`
- `--color-background`, `--color-surface`
- `--color-text`, `--color-link`, `--color-link-hover`
- `--color-border`

After changing styles, commit and push to trigger a rebuild.

## Update repository-specific config

In `_config.yml`, verify these values remain correct for this repository:

- `url: "https://lilys05.github.io"`
- `baseurl: "/comm-primer-"`

If the repository name or account changes, update both fields.

## Local preview (optional)

If you want to run locally:

1. Install Ruby and Bundler.
2. Run:

   ```bash
   bundle install
   bundle exec jekyll serve
   ```

3. Open `http://127.0.0.1:4000/comm-primer-/`
