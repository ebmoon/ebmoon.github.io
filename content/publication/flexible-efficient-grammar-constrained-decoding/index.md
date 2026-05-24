---
title: "Flexible and Efficient Grammar-Constrained Decoding"
authors:
- admin
- Timothy Zhou
- Loris D'Antoni
date: "2025-07-01T00:00:00Z"
doi: ""
publishDate: "2025-07-01T00:00:00Z"
publication_types: ["paper-conference"]
publication: "International Conference on Machine Learning 2025"
publication_short: "ICML 2025"
abstract: "This work studies flexible and efficient methods for grammar-constrained decoding."
summary: "Flexible and efficient grammar-constrained decoding."
tags:
- Large Language Models
- Constrained Decoding
featured: true
url_pdf: https://arxiv.org/abs/2502.05111
url_code: 'https://github.com/large-loris-models/alignment'
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

This paper focuses on the practical cost of grammar-constrained decoding. Grammar-constrained decoding can guarantee that generated outputs follow a context-free grammar, but efficient implementations must reconcile two different token systems: the grammar's terminals and the language model's subword tokenizer.

The work introduces a more flexible and efficient algorithm for computing the token masks needed during decoding. The main improvement is in offline preprocessing, making it faster to prepare common grammars while preserving efficient online mask computation during generation.

This is useful for structured generation tasks such as code, data formats, and other domains where syntax errors are unacceptable. The work appeared at ICML 2025.
