---
title: "Synthesizing Specifications"
authors:
- admin
- Loris D'Antoni
- Thomas Reps
date: "2023-10-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2023-10-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "Object-Oriented Programming, Systems, Languages & Applications 2023"
publication_short: "OOPSLA 2023"

abstract: "This work studies synthesis of specifications for program behavior."

# Summary. An optional shortened abstract.
summary: "A framework for synthesizing useful program specifications."

tags:
- Program Synthesis
- Program Specifications
featured: true

# links:
# - name: ""
#   url: ""
url_pdf: https://arxiv.org/abs/2301.11117
url_code: 'https://github.com/ebmoon/oopsla23-artifact'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

This paper studies how to synthesize useful formal specifications from program code. Instead of requiring a developer to manually write every property, the framework takes a query about a set of function definitions and a domain-specific language for expressing candidate properties.

The synthesized results are best properties in the chosen language: each property is as precise as possible within the language, and the set is exhaustive with respect to the query. This makes the approach useful for extracting program facts that are both formal and tailored to the kind of property a user wants to see.

The work is implemented in Spyro and demonstrates applications including program-specification mining, abstract-domain operations, and algebraic properties of program modules. It appeared at OOPSLA 2023.
