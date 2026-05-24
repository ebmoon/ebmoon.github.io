---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      headings:
        about: Summary
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`.
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false
  - block: education-list
    content:
      title: Education
      username: admin
    design:
      date_format: 'January 2006'
  - block: collection
    id: papers
    content:
      title: Selected Publications
      text: ""
      filters:
        folders:
          - publication
        featured_only: true
        exclude_featured: false
    design:
      view: citation
---
