# ReVIEW LiveReload

## Prerequisites

- Ruby 1.9.3+ and Bundler
- LiveReload extension for your web browser

## Settings

1. Clone this repository.
1. `$ bundle install --binstubs=bin --path .bundle`
1. Run web server with `$ bundle exec rake server`
1. Run guard with `$ bundle exec guard`

## How to use

`*.md` files in `markdown` dir are compiled and html files are generated in the `html` dir.

Open `http://localhost:5000` and enjoy.


