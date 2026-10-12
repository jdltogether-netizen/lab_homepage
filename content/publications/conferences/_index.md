---
title: Conferences
type: landing
summary: Conference presentations and proceedings.

# Items live as individual pages in content/publications/ and are separated
# here by publication_types. The collection block only queries Kind "page",
# so this section page never lists itself.
sections:
  - block: collection
    content:
      title: Conferences
      subtitle: ''
      text: ''
      filters:
        folders:
          - publications
        publication_type: paper-conference
      count: 0   # all
      sort_by: Date
      sort_ascending: false
    design:
      # Opt in to the year headings. The collection block cannot group, so
      # the script in layouts/_partials/hooks/head-end/jdl-style-overrides.html
      # reads each citation's year and inserts them. Opt-in by class so the
      # shorter "recent" lists elsewhere stay ungrouped. Remove this line to
      # go back to a flat list.
      css_class: "jdl-group-by-year"
      view: citation
      spacing:
        padding: ["3rem", 0, "3rem", 0]
---
