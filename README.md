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
- Images are compressed losslessly on commit by a lefthook pre-commit hook
  (`lefthook.yml`, settings in `.image_optim.yml`). Without the hook, run
  `bundle exec image_optim <files>` yourself. The same hook then runs
  `bin/check-image-sizes`, which CI (`.github/workflows/images.yml`) also runs
  on PRs: images over 256 KB fail, or 3 MB for the plate masters and mocks that
  don't ship.
- Before a push, lefthook builds the CSS and the site, then runs html-proofer
  over `_site` for broken internal links and images (external links are skipped).

## Local preview

Ruby and Node versions are pinned in `.tool-versions` (`asdf install`); CI reads
the same file. `Gemfile.lock` and `package-lock.json` are committed and CI
installs exactly what they pin; after changing the `Gemfile`, run `bundle install`
and commit the updated lock.

    npm install
    bundle install
    bundle exec lefthook install # once per clone: pre-commit and pre-push hooks
    npm run watch:css            # in one terminal
    bundle exec jekyll serve     # in another

Then open <http://localhost:4000>.
