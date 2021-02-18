# Topgrade Docs

Documentation for [Topgrade](https://github.com/r-darwish/topgrade).

This site currently uses the [hugo book](https://themes.gohugo.io//theme/hugo-book/) theme as a git submodule in `themes/book/`. An example/documentation site for the theme is at <https://themes.gohugo.io//theme/hugo-book/>

The example `config.toml` is at <https://github.com/alex-shpak/hugo-book/blob/master/exampleSite/config.toml>

To build:

- Install [hugo](https://gohugo.io/getting-started/installing/) and then either:
  - Run `hugo --minify` to build for release
  - Run `hugo serve --minify` to run a local server for development

A Github Action is setup at [`.github/hugo.yaml`](.github/hugo.yaml) to host the documentation at [Topgrade Docs](https://jasikpark.github.io/topgrade)

TODO:

- [ ] Replace example content in the blog with pertinent information.
