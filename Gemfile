source "https://rubygems.org"
# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!

gem "jekyll"
# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# gem "github-pages", group: :jekyll_plugins
gem "kramdown-parser-gfm"
gem 'jekyll-relative-links'
gem "webrick", "~> 1.7" # Ruby 3 support

# Download a theme for  Jekyll sites. Currently using custom css.
gem "minima", "~> 2.5"
gem 'jekyll-theme-minimal'
group :jekyll_plugins do
    gem "jekyll-feed", "~> 0.12"
  end
# gem "jekyll-athena"
# Windows doesn't allow hot reload without this
gem 'wdm', '>= 0.1.0' if Gem.win_platform?
# Get Timezone for Blog
# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# Add to quick make posts
gem 'jekyll-compose', group: [:jekyll_plugins]
# Post timeline sorting
gem 'jekyll-archives'
