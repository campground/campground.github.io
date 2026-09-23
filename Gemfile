source "https://rubygems.org"

# Matches the Jekyll version and plugins GitHub Pages builds with.
# Local preview: bundle install && bundle exec jekyll serve
gem "github-pages", group: :jekyll_plugins
gem "webrick"

# Lossless image compression: bundle exec image_optim -r assets
# image_optim_pack bundles the optimizer binaries (no brew/apt installs).
group :development do
  gem "image_optim"
  gem "image_optim_pack"
  # Git hooks (lefthook.yml): bundle exec lefthook install
  gem "lefthook"
end
