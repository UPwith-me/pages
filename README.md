# He Jipei Personal Homepage

This repository is a WowPage-based migration of the previous personal homepage. The old page content has been moved into a maintainable data-driven structure instead of being hard-coded across many HTML blocks.

## What was migrated

- Personal identity, contact information, GitHub profile, and author sidebar configuration
- Homepage content: About, News, Experience, Learning, Projects, Research Preparation, Contact
- Project page: GrandMaster
- Avatar images from the original site
- Original deployment settings for `https://upwith-me.github.io/pages`

## How to maintain the site

Most future edits should happen in these files:

| File | Purpose |
|---|---|
| `_data/home.yml` | Homepage text, news, experience, learning background, project cards, contact information |
| `_data/grandmaster.yml` | GrandMaster project page content |
| `_data/navigation.yml` | Top navigation items |
| `_config.yml` | Site title, author sidebar, GitHub Pages URL, repository name |
| `assets/css/home.css` | WowPage-coupled visual styling and small custom helpers |
| `images/` | Avatar, logos, and project illustrations |
| `files/` | CV or downloadable files, if added later |

To add a new project, edit `_data/home.yml` and append one item under `projects:`. The homepage will render it automatically.

To add a new homepage news item, edit `_data/home.yml` and append one item under `news:`.

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
