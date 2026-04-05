---
title: 'Projects'
date: 2024-05-19
type: landing

design:
  spacing: '5rem'

sections:
  - block: collection
    content:
      title: Featured Projects
      text: Selected open-source projects and research repositories.
      filters:
        folders:
          - project
        featured_only: true
    design:
      view: article-grid
      fill_image: false
      columns: 3
  - block: collection
    content:
      title: All Projects
      filters:
        folders:
          - project
        exclude_featured: true
    design:
      view: article-grid
      fill_image: false
      columns: 3
---
