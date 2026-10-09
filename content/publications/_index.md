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
    # id scopes the gap fix in the head-end style hook: the citation view
    # hardcodes mt-16 sm:mt-20 on its list, which left the title stranded.
    id: recent-journals
    content:
      title: Recent Journal Papers
      archive:
        # Without this the button goes to /publication_types/article-journal/,
        # the raw Hugo taxonomy page - titled "Article-Journal", paginated at
        # 10, and a worse duplicate of the curated Journals page.
        link: '/publications/journals/'
        text: 'See all journal papers'
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
