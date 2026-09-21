# campground.github.io

Source for <https://campground.github.io>, built by GitHub Pages with Jekyll.

## How it publishes

GitHub Pages builds the `master` branch with Jekyll on every push
(Settings → Pages → Build and deployment → Deploy from a branch → `master` / root).
Changes can take up to 10 minutes to appear.

## Editing

- Site title, description and theme live in `_config.yml`.
- Pages are Markdown files with front matter; `index.md` is the home page.

## Local preview

    bundle install
    bundle exec jekyll serve

Then open <http://localhost:4000>.
