---
title: "Constrained Sampling for Language Models Should Be Easy: An MCMC Perspective"
authors:
- Emmanuel Anaya Gonzalez
- Sairam Vaidya
- admin
- Ruyi Ji
- Taylor Berg-Kirkpatrick
- Loris D'Antoni
author_notes:
- "Equal contribution"
- "Equal contribution"
date: "2025-12-01T00:00:00Z"
doi: ""
publishDate: "2025-12-01T00:00:00Z"
publication_types: ["paper-conference"]
publication: "Neural Information Processing Systems 2025"
publication_short: "NeurIPS 2025"
abstract: "This work presents an MCMC perspective on constrained sampling for language models."
summary: "An MCMC perspective on constrained sampling for language models."
tags:
- Large Language Models
- Constrained Decoding
featured: false
url_pdf: https://arxiv.org/abs/2506.05754
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''
image:
  caption: ''
  focal_point: ''
  preview_only: false
projects: []
slides: ""
---

This paper studies constrained sampling for language models from an MCMC perspective. The goal is to generate outputs that satisfy hard constraints while preserving the language model's conditional distribution, instead of only forcing validity through local token masks.

The work frames constrained generation as a sampling problem over valid outputs. It constructs proposal distributions that stay inside the constrained space and uses a Metropolis-Hastings acceptance rule based on the language model likelihood. This gives a principled way to explore valid outputs while converging toward the desired conditional distribution.

The paper evaluates the approach on synthetic benchmarks and program fuzzing tasks, where both validity and diversity matter. It appeared at NeurIPS 2025.
