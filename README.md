# Ruidong Zhang — Academic Homepage

A research-oriented personal website built from the official [al-folio](https://github.com/alshedivat/al-folio) v1.2 template. The site is configured for the root GitHub Pages repository `zread258.github.io`.

## Install and preview

Docker is the recommended local workflow because it contains Ruby, Jekyll, ImageMagick, and the required gems:

```bash
docker compose up
```

Open <http://localhost:8080>. Stop the server with `Ctrl+C`, then run `docker compose down`.

For a native installation, install Ruby 3.3, Bundler, Node.js 20, npm, Python 3.12, and ImageMagick, then run:

```bash
bundle install
npm ci
bundle exec jekyll serve --livereload
```

The local native preview is available at <http://localhost:4000>.

For a production build:

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

The generated site is written to `_site/` and must not be committed.

## Content map

- Homepage: `_pages/about.md`
- Research: `_pages/research.md`
- Experience: `_pages/experience.md`
- Web CV content: `_data/cv.yml`
- Contact and optional profile links: `_data/socials.yml` and `_data/profile.yml`
- Site metadata and feature switches: `_config.yml`
- Future publication records: `_bibliography/papers.bib`

The internship-availability sentence is controlled by `internship_availability` in `_data/profile.yml`. Optional profile icons remain hidden while their URLs are empty.

## Update the CV

Edit `_data/cv.yml`, then render the public PDF with:

```bash
rendercv render _data/cv.yml --design assets/rendercv/design.yaml --locale-catalog assets/rendercv/locale.yaml --settings assets/rendercv/settings.yaml
```

The stable public file is `assets/pdf/Ruidong_Zhang_CV.pdf`. The `Render a CV` GitHub Action also regenerates it whenever the CV data or RenderCV configuration changes. Keep the public PDF consistent with the website's disclosure policy.

## Add a publication later

Only after the current anonymous-review restriction has ended:

1. add the public BibTeX record to `_bibliography/papers.bib`;
2. add any public paper, preview, code, or artifact files under `assets/`;
3. restore an al-folio Publications page in `_pages/publications.md` with `nav: true`;
4. build locally and verify all links and metadata.

The initial repository deliberately contains no publication record or hidden publication page.

## Profile photo

No portrait was supplied with this workspace, so the homepage currently uses a text-first layout. To add one, place an optimized image such as `photo.webp` in `assets/img/` and set `profile_image: photo.webp` in `_data/profile.yml`. The existing layout applies a restrained 4:5 crop, responsive sizing, and `Ruidong Zhang` alt text. Retain the original photograph separately if desired; do not commit private source material.

## GitHub Pages deployment

Push the repository to `zread258/zread258.github.io` and set Pages to deploy from the `gh-pages` branch at `/ (root)`. `.github/workflows/deploy.yml` builds the production site on pushes to `main` or `master` and publishes `_site/` to `gh-pages`.

## Remaining placeholders

- `<ORCID_URL>` in `_data/profile.yml`
- `<GOOGLE_SCHOLAR_URL>` in `_data/profile.yml`
- `<LINKEDIN_URL>` in `_data/profile.yml`, if desired
- `assets/img/photo.webp`, when a public profile photograph is supplied

The public CV filename is already set to `Ruidong_Zhang_CV.pdf`; change it consistently in `_pages/about.md`, `_pages/cv.md`, `_data/socials.yml`, RenderCV settings, and this README if a different final filename is preferred.
