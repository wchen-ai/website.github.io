---
title: ""
date: 2022-10-24
type: landing

design:
  spacing: "5rem"

sections:
  # ── Hero: Bio ──────────────────────────────────────────────
  - block: resume-biography-3
    content:
      username: admin
      text: ""
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false

  # ── Research Mission ───────────────────────────────────────
  - block: markdown
    id: research
    content:
      title: 'Research'
      subtitle: ''
      text: |-
        My research sits at the intersection of **medical imaging** and **deep learning**, with the goal of building AI systems that are accurate, fair, and deployable in real clinical workflows.

        **Current focus** — At Mayo Clinic Arizona, I am developing vision-language foundation-model pipelines to predict **Major Adverse Cardiovascular Events (MACE)** from routine non-gated chest CT and free-form clinical notes, with emphasis on embedding-bias detection and mitigation for equitable risk stratification.

        **PhD work** — During my PhD at UW-Madison I built CNN, Transformer, and diffusion-model solutions for synthetic CT generation, PET attenuation correction, tumor segmentation, and uncertainty estimation, collaborating with GE Healthcare and Erasmus MC.

        I also co-organize the [Stanford MedAI journal club](https://stanford-medai.github.io) and serve as a reviewer for leading medical-imaging venues.
    design:
      columns: '1'

  # ── Selected Publications ──────────────────────────────────
  - block: collection
    id: papers
    content:
      title: Selected Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      view: article-grid
      columns: 2

  # ── Recent Publications ────────────────────────────────────
  - block: collection
    content:
      title: Recent Publications
      text: "[View all publications &rarr;](/publication/)"
      count: 5
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation

  # ── Featured Projects / Repos ──────────────────────────────
  - block: collection
    id: projects
    content:
      title: Featured Projects
      text: "[View all projects &rarr;](/projects/)"
      filters:
        folders:
          - project
    design:
      view: article-grid
      fill_image: false
      columns: 3

  # ── Recent Blog Posts ──────────────────────────────────────
  - block: collection
    id: blog
    content:
      title: Recent Posts
      subtitle: ''
      text: "[Read more &rarr;](/post/)"
      page_type: post
      count: 3
      filters:
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
      order: desc
    design:
      view: date-title-summary
      spacing:
        padding: [0, 0, 0, 0]

  # ── Talks ──────────────────────────────────────────────────
  - block: collection
    id: talks
    content:
      title: Recent Talks
      text: "[View all talks &rarr;](/event/)"
      count: 3
      filters:
        folders:
          - event
    design:
      view: article-grid
      columns: 1
---
