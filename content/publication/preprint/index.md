---
title: "LOUD: Synthesizing Strongest and Weakest Specifications"
authors:
- admin
- Xuanyu Peng
- Loris D'Antoni
date: "2024-08-22T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-08-22T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "Specifications allow us to formally state and understand what programs are intended to do. To help one extract useful properties from code, Park et al. recently proposed a framework that given (i) a quantifier-free query posed about a set of function definitions, and (ii) a domain-specific language L in which each extracted property is to be expressed (we call properties in the language L-properties), synthesizes a set of L-properties such that each of the property is a strongest L-consequence for the query: the property is an over-approximation of query and there is no other L-property that over-approximates query and is strictly more precise than each property.
The framework by Park et al. has two key limitations. First, it only supports quantifier-free query formulas and thus cannot synthesize specifications for queries involving nondeterminism, concurrency, etc. Second, it can only compute L-consequences, i.e., over-approximations of the program behavior.
This paper addresses these two limitations and presents a framework, Loud, for synthesizing strongest L-consequences and weakest L-implicants (i.e., under-approximations of the query) for function definitions that can involve existential quantifiers.
We implemented a solver, Aspire, for problems expressed in Loud which can be used to describe and identify sources of bugs in both deterministic and nondeterministic programs, extract properties from concurrent programs, and synthesize winning strategies in two-player games."

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Program Synthesis
- Program Specifications

featured: true

# links:
# - name: Custom Link
#   url: http://example.org
url_pdf: https://arxiv.org/abs/2408.12539
url_code: 'https://github.com/ebmoon/spyro-sketch'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# image:
#   caption: ''
#   focal_point: ""
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
# - internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---

This work is an extension of my [previous paper](https://dl.acm.org/doi/10.1145/3622861) for a general framework.
