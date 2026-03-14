# Repository Guidelines

## Project Structure & Module Organization
This repository is a small Jekyll site. Primary content lives at the root in Markdown pages such as `index.markdown` and `about.markdown`. Blog posts belong in `_posts/` and must follow Jekyll naming like `YYYY-MM-DD-slug.markdown`. Site-wide settings live in `_config.yml`, and Ruby dependencies are declared in `Gemfile` and locked in `Gemfile.lock`.

`_site/` contains generated output from Jekyll. Treat it as build artifacts: verify it when needed, but do not hand-edit files there because they will be regenerated.

## Build, Test, and Development Commands
Use Bundler so the site runs against the versions pinned in `Gemfile.lock`.

- `bundle install` installs Jekyll, Minima, and plugin dependencies.
- `bundle exec jekyll serve` builds the site and starts a local dev server with auto-regeneration.
- `bundle exec jekyll build` generates the static site into `_site/`.
- `bundle exec jekyll doctor` checks for common configuration and content issues.

Run commands from the repository root.

## Coding Style & Naming Conventions
Write pages and posts in Markdown with YAML front matter at the top. Use two-space indentation in YAML, keep keys lowercase, and prefer concise values over long inline comments. Name posts with lowercase, hyphen-separated slugs, for example `_posts/2026-03-13-release-notes.markdown`.

Keep permanent pages simple and descriptive, and prefer `.markdown` for content files to match the existing repository. Do not edit generated assets in `_site/assets/`; change source content or configuration instead.

## Testing Guidelines
There is no formal test suite in this repository. The minimum validation step is `bundle exec jekyll build`; use `bundle exec jekyll doctor` before submitting larger changes. After content or layout changes, load the site locally with `bundle exec jekyll serve` and verify the affected page, links, and post dates.

## Commit & Pull Request Guidelines
This repository is initialized with Git, but it currently has no commits, so no project-specific convention can be inferred from history yet. Use short, imperative commit messages such as `Add about page copy` or `Update site title in config`.

Pull requests should include a brief summary, the reason for the change, and screenshots for visible UI or layout updates. Call out `_config.yml` changes explicitly, since they often require a server restart to verify.
