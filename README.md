# Ce Ji — academic homepage

This repository contains the bilingual English/Chinese academic homepage of Ce Ji. It is a small, self-contained Jekyll site designed for GitHub Pages.

## Structure

- English pages live at the repository root.
- Chinese counterparts live in `zh/`.
- `_data/` contains structured academic content and navigation.
- `_includes/` renders each structured content section.
- `_layouts/` contains the three shared page shells: default, home, and post.
- `assets/css/site.css` contains the complete visual design.
- `MAINTAIN.md` explains routine updates.

The site intentionally has no theme dependency, JavaScript framework, Bootstrap, or external font dependency.

## Local preview

Install the Ruby dependencies once:

```sh
bundle install
```

Then start the local site:

```sh
bundle exec jekyll serve --livereload
```

Open <http://127.0.0.1:4000>.

## Attribution

The visual direction is based on the [Academic Jekyll Theme](https://github.com/LeNPaul/academic) by Paul Le, licensed under the MIT License. The site structure and implementation have been substantially rewritten and customized for Ce Ji. See `LICENSE.txt`.
