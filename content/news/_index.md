---
title: News
type: landing
summary: Press coverage of the lab, 2016 to the present.

sections:
  - block: collection
    # Shares the landing page's block id so the #news rule in
    # layouts/_partials/hooks/head-end/jdl-style-overrides.html lays these
    # cards out two per row here too. See `columns` below.
    id: news
    content:
      title: News
      subtitle: 2016 to the present
      text: ''
      filters:
        folders:
          - news
      count: 0   # all
      sort_by: Date
      sort_ascending: false
    design:
      view: card
      # NOTE: the `card` view hardcodes a 1-column grid and ignores `columns`;
      # the 2-per-row layout comes from the #news CSS rule.
      columns: 2
      show_date: true
      show_read_time: false
      show_read_more: false
      spacing:
        padding: ["3rem", 0, "3rem", 0]
---
