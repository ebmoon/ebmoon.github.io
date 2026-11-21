# Website Editing Guide

This site is a Hugo Blox academic website. Most routine updates are made by editing Markdown files under `content/`; layout overrides live under `layouts/`.

## Common Changes

| What you want to change | File to edit | What to do |
| --- | --- | --- |
| Homepage section order | `content/_index.md` | Edit the `sections` list. |
| Bio text, interests, social links, education, work, and teaching | `content/authors/admin/_index.md` | Edit the author profile fields. The homepage and Experience page share the work, education, and teaching entries. |
| Profile photo | `content/authors/admin/avatar.jpg` | Replace the image with a new file using the same name. |
| Experience page section order | `content/experience.md` | Edit the `sections` list. |
| Homepage selected publications | `content/_index.md` and individual files in `content/publication/*/index.md` | Set `featured: true` on papers to show them on the homepage, or `featured: false` to hide them. |
| Add a new publication | `content/publication/<new-paper-slug>/index.md` | Copy an existing publication folder and update the front matter and links. Add `featured: true` only if it should appear on the homepage. |
| Navigation labels or menu items | `config/_default/menus.yaml` or `config/_default/languages.yaml` | Check these files for menu configuration before editing templates. |
| Site title, theme, footer, search, analytics | `config/_default/params.yaml` | Edit global site settings here. |
| Custom homepage bio layout | `layouts/partials/hbx/blocks/resume-biography-3/block.html` | Edit only when the template structure or styling needs to change. Prefer `content/_index.md` for text labels. |
| Custom education block layout | `layouts/partials/hbx/blocks/education-list/block.html` | Edit only when the homepage education layout needs structural or style changes. |
| Custom work and teaching layouts | `layouts/partials/hbx/blocks/work-experience/block.html` and `layouts/partials/hbx/blocks/teaching-experience/block.html` | These blocks render on both the homepage and Experience page. |

## Publication Checklist

For each publication record in `content/publication/<paper-slug>/index.md`:

1. Update `title`, `authors`, `date`, `publication`, and `publication_short`.
2. Set `abstract` and, if useful, `summary`.
3. Set `featured: true` only for homepage selected publications.
4. Add paper and artifact links under `links`. Existing `url_pdf` and `url_code` fields also work.

Publication records populate the lists without generating individual pages. Titles link to the first available paper source.

## Build And Preview

Run this from the repo root after edits:

```bash
PATH=$PWD/node_modules/.bin:$PATH hugo --gc --minify --cacheDir /private/tmp/ebmoon-hugo-cache
```

To preview the built site locally:

```bash
python3 -m http.server 8001 --directory public
```

Then open:

```text
http://127.0.0.1:8001/
```

Hugo may print deprecation warnings from Hugo Blox or old example content. The important part is that the command exits successfully.
