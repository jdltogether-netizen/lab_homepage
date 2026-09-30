---
title: Publications
type: landing
cms_exclude: true

sections:
  - block: markdown
    content:
      title: Publications
      subtitle: ''
      text: |
        The lab's written record, split by type. Journal papers, conferences and
        patents each have a page per item; lectures are listed in full on
        their own page.
    design:
      spacing:
        padding: ["3rem", 0, "0rem", 0]

  - block: collection
    content:
      title: Recent Journal Papers
      filters:
        folders:
          - publications
        publication_type: article-journal
      count: 15
    design:
      view: citation
      spacing:
        padding: ["1rem", 0, "3rem", 0]
---
