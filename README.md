# ae4292.github.io

Personal academic website for Adrian Enders, built with [Jekyll](https://jekyllrb.com/) on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) theme and hosted on GitHub Pages at [ae4292.github.io](https://ae4292.github.io/).

## Local development

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

## Structure

- `_pages/` — standalone pages (About, Research, Projects, References)
- `_publications/`, `_projects/`, `_talks/`, `_teaching/` — collection content, one file per entry
- `_data/navigation.yml` — header navigation links
- `files/` — CV and other downloadable PDFs
- `images/` — site images
- `_config.yml` — site-wide settings (title, author bio, social links, etc.)

## Deployment

Pushes to `master` are built and published automatically by GitHub Pages.
