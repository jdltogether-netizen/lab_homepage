---
title: Publications
type: landing
cms_exclude: true

sections:
  - block: markdown
    content:
      title: Publications
      subtitle: ''
      # Absolute paths, not "journals/": canonifyURLs rewrites a relative
      # link against baseURL, which would send it to the site root.
      text: |
        The lab's written record, split by type. Follow any of these for the
        full list &mdash; [journal papers](/publications/journals/),
        [conferences](/publications/conferences/) and
        [patents](/publications/patents/) each have a page per item, and
        [lectures](/publications/lectures/) are listed in full on their own
        page.
    design:
      spacing:
        padding: ["3rem", 0, "0rem", 0]

  - block: collection
    # id scopes two rules in the head-end style hook: the gap under the title
    # (the citation view hardcodes mt-16 sm:mt-20) and hiding the archive
    # button, which has no single destination now that this list is mixed.
    # `archive.enable: false` cannot do that - the template reads it through
    # `| default`, which treats false as unset and turns the button back on.
    id: recent-publications
    content:
      # No publication_type filter, so this samples every type the way the
      # home page does. Filtering it to article-journal made the hub for all
      # four types read as a journals page. The intro above links each full
      # list, which is what the archive button would otherwise have done.
      title: Recent Publications
      filters:
        folders:
          - publications
      count: 15
    design:
      view: citation
      spacing:
        padding: ["1rem", 0, "3rem", 0]
---
