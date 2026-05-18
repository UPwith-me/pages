# Personal Homepage Maintenance Guide

This project is intentionally YAML-driven. In normal maintenance, edit `_data/home.yml` and `_data/grandmaster.yml` first. Avoid editing Liquid templates unless you want to change layout behavior.

## 1. Add links inside normal text

Most text fields now support Markdown links directly:

```yml
text: "接受[宋睿华老师](https://dblp.uni-trier.de/pid/s/RuihuaSong.html)的指导。"
```

This works in:

- `hero.intro`
- `news[].text`
- `focus_cards[].text`
- `experience[].description`
- `learning.subtitle`
- `learning.groups[].items[]`
- `projects[].description`
- `projects[].bullets[]`
- `preparation.cards[].text`
- `contact.text`
- `extra_sections` text/content/items/cards
- most GrandMaster page text fields

For external links, always include `https://` or `http://`.

Good:

```yml
text: "[王文轩老师](https://jarviswang94.github.io)"
```

Avoid:

```yml
text: "[王文轩老师](jarviswang94.github.io)"
```

## 2. Add button-style links

For hero buttons, contact buttons, project links, or generic section links, use this form:

```yml
links:
  - label: "GitHub"
    url: "https://github.com/UPwith-me"
  - label: "Project Page"
    url: "/grandmaster/"
  - label: "Email"
    url: "mailto:hejipei0228@ruc.edu.cn"
```

The template now automatically handles:

- external URLs: `https://...`
- internal pages: `/grandmaster/`
- anchors: `#projects`
- email links: `mailto:...`

You usually do not need to write `external: true` anymore. You may still write it if you want, but the template can infer external links from `http://` or `https://`.

## 3. Add a new project

Edit `_data/home.yml`:

```yml
projects:
  - title: "New Project"
    subtitle: "Short label"
    image: "/images/new-project.svg"
    description: >-
      This project studies [multimodal reasoning](https://example.com).
    tags:
      - "Multimodal"
      - "Evaluation"
    bullets:
      - "First contribution with a [link](https://example.com)."
      - "Second contribution."
    links:
      - label: "GitHub Repo"
        url: "https://github.com/UPwith-me/example"
```

## 4. Add a completely new homepage section without editing HTML

Use `extra_sections` at the bottom of `_data/home.yml`.

Example: publications

```yml
extra_sections:
  - id: "publications"
    kicker: "Publications"
    title: "论文与研究产出"
    subtitle: "这里可以放论文、preprint、报告或课程项目。"
    cards:
      - title: "Paper Title"
        text: "Accepted by [Conference](https://example.com), 2026."
        links:
          - label: "PDF"
            url: "https://example.com/paper.pdf"
          - label: "Code"
            url: "https://github.com/UPwith-me/example"
```

Example: awards

```yml
extra_sections:
  - id: "awards"
    title: "Awards"
    items:
      - "2026 · Award name · [link](https://example.com)"
      - "2025 · Another award"
```

Example: a link collection

```yml
extra_sections:
  - id: "links"
    title: "Selected Links"
    content: >-
      这里可以集中放一些长期入口。
    links:
      - label: "Google Scholar"
        url: "https://scholar.google.com/"
        type: "primary"
      - label: "GitHub"
        url: "https://github.com/UPwith-me"
```

## 5. Keep YAML safe

Use quotes around text with `:` or `#`.

Good:

```yml
text: "Research focus: Multimodal LLM Reasoning"
```

For long text, prefer:

```yml
description: >-
  First sentence with [a link](https://example.com).
  Second sentence.
```

