# Lloyd Weber: Geospatial Portfolio

Source for my portfolio site, **[lweber89.github.io](https://lweber89.github.io)**, which highlights my geospatial data engineering and analysis work.

## What's on the site

- **Home, Experience, Publications, and Contact** pages, plus a downloadable CV.
- **Projects:**
  - [geocrime-stl](https://github.com/lweber89/geocrime-stl): an open-source Python ETL package for St. Louis crime data, published on [PyPI](https://pypi.org/project/geocrime-stl/).
  - [St. Louis Crime Data Explorer](https://lweber89.github.io/geocrime-stl/dashboard/): an interactive dashboard built on that package.

## How it's built

The site is a static [MkDocs](https://www.mkdocs.org/) project using the [Material theme](https://squidfunk.github.io/mkdocs-material/).

- Pages are Markdown files in `docs/`; site settings and navigation are in `mkdocs.yml`.
- Pushing to `main` runs the GitHub Actions workflow in `.github/workflows/deploy.yml`, which builds the site and publishes it to the `gh-pages` branch.

## Run locally

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open <http://127.0.0.1:8000>. If you prefer conda, `conda env create -f environment.yml` creates an equivalent environment named `portfolio`.

## Adding a project

1. Copy an existing page in `docs/projects/` and edit it.
2. Add it to the `nav` section of `mkdocs.yml`.
3. Add a card for it in `docs/projects/index.md`.

## Credits and license

The site structure and theme setup started from the [Geospatial Portfolio Website Template](https://courses.spatialthoughts.com/geospatial-portfolio-workshop.html) from Spatial Thoughts, used under its MIT license (see [LICENSE](LICENSE)). The written content, CV, and images on the site are my own and all rights are reserved.
