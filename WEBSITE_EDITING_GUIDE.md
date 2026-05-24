# Website Editing Guide

This site is a Hugo Blox academic website. Most routine updates are made by editing Markdown files under `content/`; layout overrides live under `layouts/`.

## Common Changes

| What you want to change | File to edit | What to do |
| --- | --- | --- |
| Homepage section order or titles | `content/_index.md` | Edit the `sections` list. The bio block, education list, and selected publications block are configured here. |
| "Summary" heading on the homepage | `content/_index.md` | Edit `sections[0].content.headings.about`. |
| Bio text, interests, social links, education, work entries | `content/authors/admin/_index.md` | Edit the author profile fields. This data feeds the homepage bio and education list. |
| Profile photo | `content/authors/admin/avatar.jpg` | Replace the image with a new file using the same name. |
| Experience page | `content/experience.md` | Edit the `experience` and `teaching-experience` sections. Teaching is a separate category on this page. |
| Homepage selected publications | `content/_index.md` and individual files in `content/publication/*/index.md` | The homepage publication section uses `featured_only: true`. Set `featured: true` on papers to show them on the homepage, or `featured: false` to hide them. |
| Add a new publication | `content/publication/<new-paper-slug>/index.md` | Copy an existing publication folder, update the front matter, abstract, links, and body description. Add `featured: true` only if it should appear on the homepage. |
| Edit a paper page description | `content/publication/<paper-slug>/index.md` | Edit the Markdown body below the second `---`. The metadata above it controls title, authors, venue, links, and whether it is featured. |
| Navigation labels or menu items | `config/_default/menus.yaml` or `config/_default/languages.yaml` | Check these files for menu configuration before editing templates. |
| Site title, theme, footer, search, analytics | `config/_default/params.yaml` | Edit global site settings here. |
| Custom homepage bio layout | `layouts/partials/hbx/blocks/resume-biography-3/block.html` | Edit only when the template structure or styling needs to change. Prefer `content/_index.md` for text labels. |
| Custom education block layout | `layouts/partials/hbx/blocks/education-list/block.html` | Edit only when the homepage education layout needs structural or style changes. |
| Custom teaching block layout | `layouts/partials/hbx/blocks/teaching-experience/block.html` | Edit only when the teaching section layout on the Experience page needs structural or style changes. |

## Publication Checklist

For each publication page in `content/publication/<paper-slug>/index.md`:

1. Update `title`, `authors`, `date`, `publication`, and `publication_short`.
2. Set `abstract` and, if useful, `summary`.
3. Set `featured: true` only for homepage selected publications.
4. Add `url_pdf`, `url_code`, or other links.
5. Write the readable paper description below the front matter.

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
