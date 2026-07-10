# Maintaining the website

The site separates content by subject. Most updates require editing one Markdown or YAML file and do not require touching HTML.

## Common edits

| Content | File |
| --- | --- |
| English biography | `index.md` |
| Chinese biography | `zh/index.md` |
| Publications | `_data/publications.yml` |
| Education and employment | `_data/cv.yml` |
| Talks, visits, and organized events | `_data/activities.yml` |
| Contact details | `_data/contact.yml` |
| Navigation links | `_data/navigation.yml` |
| Translated headings and interface text | `_data/ui.yml` |
| Colors, spacing, and responsive design | `assets/css/site.css` |

## Bilingual data

In `cv.yml`, `activities.yml`, and `contact.yml`, translated fields use adjacent `en` and `zh` values:

```yaml
title:
  en: Postdoctoral Fellow
  zh: 博士后
```

Keeping both translations in the same record makes omissions and mismatched dates easier to notice.

Publication titles, author names, venues, and links are shared by both languages. Set `featured: true` to display a publication on the home pages.

## Add an update

Create two files in `_posts/`, one for each language. Use the same date and reciprocal `alternate_url` values:

```yaml
---
layout: post
title: "English title"
lang: en
permalink: /updates/short-name/
alternate_url: /zh/updates/short-name/
---
```

The Chinese version uses `lang: zh`, the `/zh/updates/.../` permalink, and points back to the English URL.

## Add a new page

Create one root page and one page under `zh/`. Each page needs a language, permanent URL, and counterpart URL:

```yaml
---
layout: default
title: Page title
lang: en
permalink: /page-name/
alternate_url: /zh/page-name/
---
```

Add the navigation labels and URLs to `_data/navigation.yml` if the page should appear in the header.

## Check before publishing

Run:

```sh
bundle exec jekyll build
bundle exec jekyll serve
```

Check `/`, `/publications/`, `/cv/`, `/activities/`, `/contact/`, and their `/zh/` counterparts. Test the language switch on every page and check the site at both desktop and phone widths.
