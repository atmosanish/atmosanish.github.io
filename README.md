# atmosanish.github.io

Personal research website of Anish Kumar, served at https://atmosanish.github.io.

## How it is published

GitHub Pages builds this repository with Jekyll on every push to `main`
(Settings → Pages → Build and deployment → **Deploy from a branch**, `main`, `/ (root)`).
There is nothing to install or build locally.

Keep it that way:
- do not add a `.nojekyll` file;
- do not add a "static content" deployment workflow under `.github/workflows/`.

Either one stops Jekyll from running, and the pages then show raw template code.

## Everyday edits

| To change | Edit |
|---|---|
| News | `_data/news.yml`. Empty for now, so News is hidden everywhere; the first item switches on the menu entry, the home-page block and the News page |
| Publication | `_data/publications.yml`: add at the top of its group; `selected: true` puts it on the home page |
| Talk or training | `_data/talks.yml` |
| Dataset or code | `_data/datasets.yml`: the "Data & Code" menu entry appears with the first entry |
| Location, position, profile links | `author:` block in `_config.yml` |
| Reviewer line on the CV page | `reviewer_for:` in `_config.yml` |
| CV PDF | replace `Anish_Kumar_CV.pdf` (same file name). Never include a phone number |
| Home page text | `index.html` |
| Research themes | `research.html` (instructions for adding a figure are at the top) |
| Teaching | `teaching.html` |
| Positions, education, skills | `cv.html` |
| Colours and fonts | `assets/css/main.css` |

YAML is sensitive to indentation: copy an existing entry and change its values.
Text containing a colon must stay inside quotes.

## Files

```
_config.yml          site settings and profile
_data/               news, publications, talks, datasets, navigation
_includes/           page parts (head, masthead, sidebar, footer, list items)
_layouts/            page frames
assets/css/main.css  all styling
assets/fonts/        self-hosted fonts (no requests to Google; SIL Open Font License)
images/              portrait, social-media preview image, favicon
Anish_Kumar_CV.pdf   CV download
index.html, news.html, research.html, publications.html, data.html,
talks.html, teaching.html, cv.html, 404.html, sitemap.xml, robots.txt
```

## Optional: preview on your computer

Needs Ruby. Run `gem install jekyll -v 3.10.0 kramdown-parser-gfm webrick`,
then `jekyll serve` in this folder and open http://localhost:4000.

## Custom domain later

Add the domain under Settings → Pages, then change `url:` in `_config.yml`.
