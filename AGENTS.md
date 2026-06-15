# Repository Guidelines

## Project Structure & Module Organization

This is a Jekyll-based Academic Pages site. Site-wide settings live in `_config.yml`; navigation and author metadata are in `_data/`. Page content is organized under `_pages/`, while collection content uses `_publications/`, `_talks/`, `_teaching/`, `_portfolio/`, and `_posts/`. Shared templates are in `_layouts/` and `_includes/`; styles are in `_sass/` with the entry point at `assets/css/main.scss`. Static images and icons belong in `images/`, downloadable PDFs and other public files in `files/`, and JavaScript in `assets/js/`. Scripts and notebooks for generating markdown content live in `markdown_generator/` and `scripts/`.

## Build, Test, and Development Commands

- `bundle install`: install Ruby and Jekyll dependencies. If system permissions fail, run `bundle config set --local path 'vendor/bundle'` first.
- `bundle exec jekyll serve -l -H localhost`: run the site locally at `http://localhost:4000` with live reload.
- `bundle exec jekyll build`: build the static site and catch template/configuration errors.
- `npm install`: install JavaScript build dependencies.
- `npm run build:js`: regenerate `assets/js/main.min.js` from vendored scripts and `assets/js/_main.js`.
- `docker compose up`: alternative local preview using the provided Docker setup.

## Coding Style & Naming Conventions

Use Markdown front matter consistently for pages and collection items. Keep filenames date-prefixed where Jekyll expects dates, for example `_posts/YYYY-MM-DD-title.md` and `_publications/YYYY-MM-DD-title.md`. Prefer two-space indentation in YAML and Liquid templates. Keep custom includes small and reusable, and avoid editing minified assets directly; update source JavaScript and run `npm run build:js`.

## Testing Guidelines

There is no dedicated unit test suite. Validate changes by running `bundle exec jekyll build` before committing. For visual or content changes, also preview locally with `bundle exec jekyll serve -l -H localhost` and check affected pages, navigation, images, and file links. If generated content changes, verify the output markdown rather than only the generator script.

## Commit & Pull Request Guidelines

Recent commits use short, imperative summaries such as `fix some err`, `update yml`, and `Migrate to academicpages template`. Keep commit subjects concise and focused on one logical change. Pull requests should include a brief description, affected pages or collections, screenshots for visual changes, and any build command used for verification. Link related issues when available.

## Security & Configuration Tips

Do not commit private keys, unpublished personal data, or local build output. Keep public assets intentional: anything in `files/`, `images/`, or generated site output may be publicly accessible. Review `_config.yml` carefully when changing URLs, analytics, author information, or GitHub Pages settings.
