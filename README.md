# campground.github.io

Source for <https://www.campgrounddd.com>, built by GitHub Pages with Jekyll.

## How it publishes

A GitHub Actions workflow (`.github/workflows/pages.yml`) runs on every push to
`master`: it compiles Tailwind CSS, builds the site with Jekyll, and deploys to
GitHub Pages. This needs Settings → Pages → Build and deployment → Source set
to **GitHub Actions**.

## Editing

- Site title and description live in `_config.yml`.
- Pages are Markdown files with front matter; `index.html` is the home page.
- Layouts live in `_layouts/`.
- The Tailwind theme (brand colors) lives in `_tailwind/site.css`. It compiles
  to `assets/css/site.css`, which is git-ignored.
- Design context lives in `PRODUCT.md`.

## Local preview

Ruby and Node versions are pinned in `.tool-versions` (`asdf install`); CI reads
the same file. `Gemfile.lock` and `package-lock.json` are committed and CI
installs exactly what they pin; after changing the `Gemfile`, run `bundle install`
and commit the updated lock.

    npm install
    bundle install
    npm run watch:css            # in one terminal
    bundle exec jekyll serve     # in another

Then open <http://localhost:4000>.
