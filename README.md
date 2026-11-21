# Jipei He Personal Homepage

This is a Jekyll academic homepage hosted on GitHub Pages.

## What was migrated

- Personal identity, contact information, GitHub profile, and author sidebar configuration
- Homepage content: research introduction, selected publications, research direction, and experience
- Project page: GrandMaster
- Avatar images from the original site
- Original deployment settings for `https://upwith-me.github.io/pages`

## How to maintain the site

Most future edits should happen in these files:

| File | Purpose |
|---|---|
| `_pages/about.md` | Homepage introduction, publications, research direction, and experience |
| `_data/grandmaster.yml` | GrandMaster project page content |
| `_data/navigation.yml` | Top navigation items |
| `_config.yml` | Site title, author sidebar, GitHub Pages URL, repository name |
| `_layouts/academic.html` and `assets/css/academic.css` | Academic homepage layout and styling |
| `images/` | Avatar, logos, and project illustrations |
| `files/` | CV or downloadable files, if added later |

To add a CV, put the PDF under `files/`, then add a navigation item in `_data/navigation.yml`, for example:

```yml
- title: "CV"
  url: "/files/your_cv.pdf"
```

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then open the local URL printed by Jekyll.

## GitHub Pages deployment

This project keeps:

```yml
url: "https://upwith-me.github.io"
baseurl: "/pages"
repository: "UPwith-me/pages"
```

So it is configured for the repository `UPwith-me/pages` and should publish at:

```text
https://upwith-me.github.io/pages
```

If you later rename the repository or use a user homepage repository like `UPwith-me.github.io`, update `baseurl` accordingly.

## Note about bundled icon fonts

This packaged copy intentionally does not include local font binaries from the template bundle. If you want the original Font Awesome / Academicons icon fonts, restore them from your own local copy of the source template or install them through your normal dependency workflow.
