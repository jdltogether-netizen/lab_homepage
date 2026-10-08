---
title: Our Team
cms_exclude: true
type: landing

sections:
  # Same block and the same group names as the homepage `#team` section, so
  # the two never drift. Adding a member means adding one file under
  # data/authors/ plus a content/authors/<slug>/_index.md for their page.
  #
  # This page must NOT fall back to Hugo's taxonomy term listing: /authors/ is
  # also where every publication co-author gets a term page, so the default
  # listing showed 270+ names as if they were lab members.
  - block: team-showcase
    id: team
    content:
      title: Our Team
      subtitle: ''
      text: ''
      user_groups:
        - Principal Investigators
        - Postdoctoral Researchers
        - PhD Students
        - Master Students
        - Interns
        - Research Staff
      sort_by: 'Params.last_name'
      sort_ascending: true
    design:
      show_role: true
      show_organizations: true
      show_interests: true
      show_social: true
      spacing:
        padding: ["3rem", 0, "3rem", 0]
---
