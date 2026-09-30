---
# Leave the homepage title empty to use the site title
title: Homepage
date: 2026-05-01
type: landing

# Browser tab title for this page ({brand} = hugoblox.seo.title)
seo:
  title: Welcome to Just Do it Lab

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: hero
    id: about
    content:
      # The hero block has no image field, so the logo goes into `title` as
      # raw HTML (the project enables unsafe HTML in Goldmark).
      # Sizing uses INLINE STYLES, not Tailwind classes: this block renders
      # client-side via Preact, so its markup never reaches hugo_stats.json
      # and Tailwind would never emit CSS for classes written here.
      # The image lives in static/media/ so the path stays literal.
      title: |
        <img src="/media/me-logo.png" alt="KAIST Mechanical Engineering" style="display:block;margin:0 auto 1.5rem;height:4rem;width:auto" />
        <span style="display:block;font-size:0.5em;line-height:1.2;letter-spacing:0.01em;color:var(--color-primary-500);margin-bottom:1.75rem">Just Do it Lab</span>
        <span style="display:block">Convergence Technology: From Rigorous Research to Real Ventures</span>
      text: |
        JDL is an Open Lab at KAIST Mechanical Engineering for convergence technology and commercialization, spanning additive manufacturing, semiconductor convergence processes, and AI-driven autonomous drone production. We work with research institutes, companies, investors, legal advisors, and global start-ups so the work leaves the bench: our researchers and students carry their projects through to global start-up ventures, during their degree and after.
      primary_action:
        text: Join Our Team
        url: '#team'
        icon: hero/user-group
      secondary_action:
        text: View Publications
        url: '#publications'
        icon: hero/academic-cap
      announcement:
        text: "Now hiring PhD students, Master’s students, and postdocs!"
        link:
          text: "Apply now"
          url: "/opportunities"
    design:
      # For full-screen, add `min-h-screen` below
      css_class: ""
      background:
        # Option A: Modern gradient mesh (recommended for 2025/2026)
        gradient_mesh:
          enable: true
          style: "waves"
          animation: "pulse"
          intensity: "medium"
          colors:
            - "primary-500/30"
            - "blue-600/20"
            - "indigo-600/15"
        
        # Option B: Team/lab image (uncomment to use instead of gradient mesh)
        # image:
        #   filename: "team-lab-hero.jpg"
        #   filters:
        #     brightness: 0.6
        #     contrast: 1.1

  - block: stats
    content:
      # Figures are rounded DOWN from the migrated content and carry a "+" so
      # they stay true as the record grows. Actual counts as of this commit,
      # from content/publications/ after de-duplication: 144 journal papers,
      # 90 conference papers, 10 patents, plus 153 lectures from
      # data/publications/lectures.json and 33 projects from
      # data/projects/jdl-projects.json.
      # NB the papers tile is 140+, not 150+: 20 entries in the legacy
      # papers.json were conference proceedings and 17 were duplicates of
      # entries in conferences.json.
      items:
        - statistic: "10+"
          description: Patents filed across Korea, Singapore, the USA, and China
          sub_metric: Three licensed. Covering energy conversion devices, label-free optical biosensors, continuously varied infill strategies for 3D printing, and PM2.5 sensor calibration.
          icon: hero/document-text
        - statistic: "150+"
          description: Plenary, keynote, and invited lectures delivered worldwide
          sub_metric: 36 plenary and keynote addresses plus 117 invited talks at international conferences, partner universities, and industry forums.
          icon: hero/user-group
        - statistic: "30+"
          description: Funded research projects led as Principal Investigator
          sub_metric: Backed by 23 sponsors — MSIT, MOTIE, NRF, KIAT, NIPA and KRIT in Korea; Samsung, LG, Google and Rolls-Royce in industry; A*STAR and Singapore MOE overseas.
          icon: hero/currency-dollar
        - statistic: "240+"
          description: Publications across journals, conferences, and patents
          sub_metric: 144 peer-reviewed journal papers, 90 conference papers, and 10 patents since 2006, spanning additive manufacturing, MEMS and microfluidic sensors, semiconductor convergence processes, energy devices, and AI-driven quality control.
          icon: hero/beaker
    design:
      layout: cards
      # Section background color (CSS class)
      css_class: "bg-gradient-to-b from-primary-50 to-white dark:from-primary-900/20 dark:to-gray-800"
      spacing:
        padding: ["3rem", 0, "3rem", 0]

  - block: research-areas
    content:
      title: Research Focus Areas
      subtitle: Pioneering AI-Driven Next-Generation Manufacturing
      text: Our research integrates artificial intelligence, advanced additive manufacturing, and autonomous systems to transform how complex products are designed, optimized, and produced in real-world environments. The work runs the full depth of the stack, from resin and nanocomposite chemistry, through the physics of the printing process and in-line quality control, up to the autonomous production systems that put it to work.
      # Per-area metrics, all hand-maintained (the block renders them as
      # literal strings - nothing here is counted automatically):
      #   team_size    - headcount working in the area
      #   publications - papers matched by topic keywords over the 170 in
      #                  data/publications/papers.json
      #   funding      - grant count, or an amount where one is known
      # Per-area `cta` links stay omitted: the Research sub-pages they would
      # point to do not exist yet.
      items:
        - name: Additive Manufacturing Processes & Functional Materials
          description: Advancing vat photopolymerization, digital light processing, material extrusion, and directed energy deposition, from the resin and nanocomposite chemistry up to real-time control of the process as it prints.
          icon: hero/cube-transparent
          gradient: from-green-400 to-emerald-600
          status: active
          topics:
            - Vat Photopolymerization
            - DLP Porous Ceramics
            - Directed Energy Deposition
            - In-Process Monitoring & Control
            - Cellulose Nanocrystals & Nanocomposites
            - Self-Healing Printable Materials
          team_size: "11+"
          publications: "28+"
          funding: "10+ grants"

        - name: Physical AI for Autonomous Manufacturing
          description: Building AI that can run a process, not just describe one. Large language and vision models read machine and sensor data, capture the tacit know-how of experienced operators, and close the control loop on additive manufacturing without a human at every step.
          icon: hero/cpu-chip
          gradient: from-blue-400 to-indigo-600
          status: active
          topics:
            - Industrial AI Agents
            - LLM & Vision-Language Models
            - Physical AI
            - Closed-Loop Process Control
            - In-Line Anomaly Detection
            - Digital Twins
            - Human-AI Collaboration
          team_size: "4+"
          publications: "3+"
          funding: "1 grant"

        - name: Next-Generation Drone Production
          description: Rethinking how a drone is built. We print a flat 2D sheet that deploys into a functional 3D airframe, so aircraft can be produced at low cost and high rate, and made where they are needed rather than shipped there.
          icon: hero/rocket-launch
          gradient: from-purple-400 to-pink-600
          status: emerging
          topics:
            - 2D Sheet to 3D Structure
            - Folding-Inspired Deployable Architectures
            - 4D Printing & Shape Memory Polymers
            - On-Demand Distributed Production
            - Low-Cost High-Rate Manufacturing
            - Attritable Airframes
          team_size: "7+"
          publications: "1+"
          funding: "$350K+"
      cta:
        text: Active Research Projects
        url: /#projects
        icon: hero/arrow-right
    design:
      layout: cards
      css_class: "bg-gradient-to-b from-gray-50 to-white dark:from-gray-900 dark:to-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]

  - block: cta-image-paragraph
    content:
      # `title` and `text` run through RenderString, so Markdown works here
      # (unlike research-areas, which escapes its strings).
      #
      # Keep each panel's copy roughly as tall as its image: the two columns
      # are centred against each other, so text that overruns the photo leaves
      # it stranded in the middle. Rough budget at a 551px column - title two
      # lines ~105px, each paragraph line ~26px, each feature line ~24px,
      # button ~75px. Image heights at that width: yellow room 551 (1:1),
      # partners 381, group photo 373, drone 366.
      items:
        - title: 'State-of-the-Art Research Environment'
          text: |
            JDL runs its own fabrication, characterization, and compute rather than queuing for shared facilities. Students design, print, process, and measure in house across KAIST, KPU, and NTU's Singapore Centre for 3D Printing, and GPU capacity grows with every new grant.
          image: facilities/kpu-08-yellow-room.jpg
          feature_icon: hero/check-circle
          features:
            - 'Additive Manufacturing: DLP and FDM printers, in-house filament fabrication, UV curing, two-photon polymerization'
            - 'Thin-Film & Semiconductor: ALD, PLD, sputtering, e-beam evaporation, PECVD, deep reactive ion etching, yellow room'
            - 'Characterization: confocal microscopy, SEM, X-ray diffraction, impedance spectroscopy, tensile testing'
            - 'AI Computing: RTX 5090 nodes, RTX A-series workstations, NAS storage, National AI Computing Center capacity'
          button:
            text: 'Virtual Lab Tour'
            url: '/facilities'

        - title: 'From Lab Bench to Production Line'
          text: |
            The drone work now has a company behind it. [KEONIX Labs](https://keonix.co.kr), a KAIST faculty start-up, is taking the lab's manufacturing research into real production.
          image: research/drone-2d-to-3d.jpg
          feature_icon: hero/rocket-launch
          features:
            - 'Pocheon Center: a civil-military-government site for drone education and production'
            - 'Printers, training programs, and custom FPV drone builds'
            - 'With Chung-Ang, Jeonbuk National and Incheon National faculty, and KAIST InnoCORE PRISM-AI'

        - title: 'Collaborative Innovation Culture'
          text: |
            JDL is an Open Lab: research institutes, companies, investors, legal advisors, and global start-ups work alongside the group, so a project can become a venture without ever leaving it.
          image: partners/jdl-partners-overview.webp
          feature_icon: hero/users
          features:
            - '23 sponsors across government, industry, and overseas agencies'
            - 'A network spanning KAIST and NTU Singapore, with KRISS, KIMM, and ETRI'
            - 'A Global Start-up Platform that carries student projects into ventures'
          button:
            text: 'Join Our Community'
            url: '/opportunities'

        - title: 'A Lab That Works Together'
          text: |
            JDL is small enough that everyone knows what everyone else is building. Postdocs and senior students pick up the newer members, and the group meets, eats, and gets out of the building together.
          image: current-members/group-hero.jpg
          feature_icon: hero/heart
          features:
            - 'Help across disciplines: mechanical engineering, computer science, electrical engineering, and materials sit side by side'
            - 'An open door: ask, and you get time on your problem'
            - 'Biweekly Friday group meetings, and lab outings through the year'
          button:
            text: 'Meet the Team'
            url: '/#team'
    design:
      css_class: "bg-white dark:bg-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]

  - block: team-showcase
    id: team
    content:
      title: Meet Our Team
      subtitle: 'World-class researchers pushing the boundaries of science & engineering technologies'
      text: 'Our multidisciplinary team works across vat photopolymerization, digital light processing, material extrusion, and directed energy deposition, from the resin and nanocomposite chemistry up to real-time control of the process as it prints, and on to AI-driven manufacturing automation and next-generation on-site drone production.'
      # Group names must match `user_groups` in data/authors/*.yaml exactly.
      user_groups:
        - Principal Investigators
        - Postdoctoral Researchers
        - PhD Students
        - Master Students
        - Interns
        - Research Staff
      sort_by: 'Params.last_name'
      sort_ascending: true
      cta:
        text: View All Team Members
        url: /authors
        icon: user-group
    design:
      show_role: true
      show_organizations: true
      show_interests: true
      show_social: true
      # Section background color
      css_class: "bg-gray-50 dark:bg-gray-900"
      # Reduce spacing
      spacing:
        padding: ["3rem", 0, "0rem", 0]

  # ── HIDDEN: Active Research Projects ────────────────────────────────
  # Still listing the template's sample content under content/projects/
  # and content/publications/. Re-enable once the real records are in.
  # ──────────────────────────────────────────────────────────────────────
#  - block: collection
#    id: projects
#    content:
#      title: Active Research Projects
#      subtitle: ''
#      text: ''
#      filters:
#        folders:
#          - projects
#      count: 0  # Number of items to show (0 = all)
#      # Default filter UI (for future release)
#      #default_button_index: 0
#      # Filter toolbar (optional)
#      # Add or remove as many filters as you like
#    #   buttons:
#    #     - name: All
#    #       tag: '*'
#    #     - name: Machine Learning
#    #       tag: ML
#    #     - name: Biology
#    #       tag: Biology
#    #     - name: Materials
#    #       tag: Materials
#    design:
#      view: article-grid
#      columns: 2
#      spacing:
#        padding: ["5rem", 0, "0rem", 0]

  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
      # Newest first; the full list lives at /publications/.
      count: 10
    design:
      view: citation
      spacing:
        padding: ["3rem", 0, "0rem", 0]

  # ── HIDDEN: Featured Research ───────────────────────────────────────
  # Still listing the template's sample content under content/projects/
  # and content/publications/. Re-enable once the real records are in.
  # ──────────────────────────────────────────────────────────────────────
#  - block: collection
#    id: featured
#    content:
#      title: Featured Research
#      filters:
#        folders:
#          - publications
#        featured_only: true
#    design:
#      view: article-grid
#      columns: 2
#      spacing:
#        padding: ["5rem", 0, "0rem", 0]

  # ── HIDDEN ───────────────────────────────────────────────────────────────
  # Events: the template ships sample events (content/events/). Re-enable once
  #   real lab events exist, and restore the Events entry in menus.yaml.
  # News: sourced from content/blog/, which is still template sample posts.
  #   The 34 real news items from the legacy site land here later; restore the
  #   News entry in menus.yaml at the same time.
  # ─────────────────────────────────────────────────────────────────────────
#  - block: collection
#    id: events
#    content:
#      title: Events
#      subtitle: Join Us for Research Presentations & Seminars
#      text: Stay connected with our research community through talks, workshops, and collaborative events
#      filters:
#        folders:
#          - events
#        exclude_past: false  # Show both past and future events
#      count: 3
#      sort_by: Date
#      sort_ascending: false
#    design:
#      view: card
#      # columns: 3
#      show_date: true
#      show_read_time: false
#      show_read_more: true
#      css_class: "bg-gradient-to-b from-white to-gray-50 dark:from-gray-800 dark:to-gray-900"
#      spacing:
#        padding: ["4rem", 0, "4rem", 0]
#
#  - block: collection
#    id: news
#    content:
#      title: Lab News & Updates
#      subtitle: ''
#      text: ''
#      # Page type to display. E.g. post, talk, publication...
#      page_type: blog
#      # Choose how many pages you would like to display (0 = all pages)
#      count: 3
#      # Filter on criteria
#      filters:
#        author: ''
#        category: ''
#        tag: ''
#        exclude_featured: false
#        exclude_future: false
#        exclude_past: false
#        publication_type: ''
#      # Choose how many pages you would like to offset by
#      offset: 0
#      # Page order: descending (desc) or ascending (asc) date.
#      order: desc
#    design:
#      # Choose a layout view
#      view: card
#      columns: 1
#      spacing:
#        padding: ["0rem", 0, "0rem", 0]
      

  # ── HIDDEN: Collaborators & Partners ─────────────────────────────────────
  # Superseded, not pending: the partner logos already appear in the
  # "Collaborative Innovation Culture" panel above, as one image carrying
  # both the global partners and the research centres. Re-enable this block
  # only if those logos should become individually linkable, in which case
  # drop the image from that panel so the two do not repeat.
  # The entries below are still the template's placeholders (MIT, Stanford,
  # Google Research); the real list is in the legacy jdl-partners.json.
  # ─────────────────────────────────────────────────────────────────────────
  # - block: logos
  #   content:
  #     title: Collaborators & Partners
  #     subtitle: Leading the way together
  #     text: We work with top universities, research institutes, and industry leaders to advance scientific discovery
  #     logos:
  #       - name: MIT
  #         image: partners/placeholder-logo.svg
  #         url: https://mit.edu
  #         external: true
  #         description: Massachusetts Institute of Technology
  #       - name: Stanford University
  #         image: partners/placeholder-logo.svg
  #         url: https://stanford.edu
  #         external: true
  #         description: Stanford Research Collaboration
  #       - name: Google Research
  #         image: partners/placeholder-logo.svg
  #         url: https://research.google
  #         external: true
  #         description: AI & Machine Learning Partnership
  #       - name: National Science Foundation
  #         image: partners/placeholder-logo.svg
  #         url: https://nsf.gov
  #         external: true
  #         description: Research Funding Partner
  #       - name: Microsoft Research
  #         image: partners/placeholder-logo.svg
  #         url: https://www.microsoft.com/research
  #         external: true
  #         description: Computing Research Collaboration
  #       - name: NIH
  #         image: partners/placeholder-logo.svg
  #         url: https://nih.gov
  #         external: true
  #         description: National Institutes of Health
  #     cta:
  #       text: Become a Partner
  #       url: /#contact
  #       icon: hero/user-plus
  #   design:
  #     display_mode: grid
  #     show_pattern: false
  #     css_class: "bg-gradient-to-b from-white to-gray-50 dark:from-gray-800 dark:to-gray-900"
  #     spacing:
  #       padding: ["4rem", 0, "4rem", 0]

  - block: contact-info
    id: contact
    content:
      title: Contact Us
      subtitle: Get in touch with our team
      visit_title: Visit Our Lab
      connect_title: Connect With Us
      address:
        lines:
          - Just Do It Lab (N7-4, Level 4, Room 4118)
          - Department of Mechanical Engineering
          - Korea Advanced Institute of Science & Technology
          - 291 Daehak-ro, Yuseong-gu
          - Daejeon 34141
          - Republic of Korea
      office_hours:
        - "Monday - Friday: 9:00 AM - 6:00 PM"
        - "Lab Meetings: Fridays 1:00 PM, biweekly"
      email: jdltogether@gmail.com
      #phone: "+1 (555) 123-4567"
      social:
        - icon: brands/linkedin
          url: https://www.linkedin.com/company/just-do-it-lab/
        - icon: brands/github
          url: https://github.com/jdltogether-netizen
      prospective:
        title: Prospective Members
        text: Interested in joining our division or lab? We're always looking for motivated talents at all levels.
        button:
          text: View Open Positions
          url: /opportunities
      map_url: https://maps.app.goo.gl/Q25Dqqc9yrj5MMSi8
      show_form: false
    design:
      css_class: "bg-gradient-to-b from-gray-50 to-white dark:from-gray-900 dark:to-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]

  # - block: cta-card
  #   content:
  #     title: Join Us!
  #     text: We are always looking for talented and motivated researchers! We have openings for PhD & Master students, Postdoc, and Research scientists.
  #     button:
  #       text: View Open Positions
  #       url: /opportunities
  #   design:
  #     card:
  #       # Card background color (CSS class)
  #       css_class: 'bg-primary-300 dark:bg-primary-700'
  #       css_style: ''
---