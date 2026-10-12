---
# Leave the homepage title empty to use the site title
title: Homepage
date: 2026-05-01
type: landing

# Browser tab title for this page ({brand} = hugoblox.seo.title)
seo:
  title: Just Do it Lab

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
      # The image lives in static/media/ so the path stays literal, and the
      # path is RELATIVE on purpose. canonifyURLs cannot reach inside this
      # block: the hero ships as a JSON payload that Preact renders, so an
      # absolute /media/... stayed at the domain root and 404'd under the
      # GitHub Pages sub-path. The hero only ever appears on the home page,
      # so a relative path resolves correctly both locally and deployed.
      title: |
        <a href="https://me.kaist.ac.kr/" target="_blank" rel="noopener" title="KAIST Department of Mechanical Engineering" style="display:block;width:max-content;margin:0 auto 1.5rem"><img src="media/me-logo.png" alt="KAIST Department of Mechanical Engineering" style="display:block;height:4rem;width:auto" /></a>
        <span style="display:block">Just Do it Lab</span>
      text: |
        JDL, in the Department of Mechanical Engineering at KAIST, focuses on additive manufacturing, AI foundation models, and core drone technologies. We collaborate with universities, research institutes, and industry partners on research and technology development.
      # Three distinct destinations in the hero: the announcement above
      # already sends people to /opportunities, so this button points at the
      # research instead of repeating it. Swap back to "Join Our Team" ->
      # /opportunities if recruiting should lead.
      primary_action:
        text: Explore Our Research
        url: 'research/'
        icon: hero/beaker
      secondary_action:
        text: View Publications
        url: '#publications'
        icon: hero/academic-cap
     # announcement:
      #  text: "Now hiring PhD students, Master’s students, and postdocs!"
       # link:
        #  text: "Apply now"
          # Relative, like every other URL in this block: the hero ships as a
          # JSON payload that Preact renders in the browser, so Hugo never
          # rewrites these and an absolute /opportunities lands at the domain
          # root - a 404 under the GitHub Pages sub-path. The hero is only on
          # the home page, so relative resolves correctly everywhere.
         # url: "opportunities/"
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
    design:
      css_class: "bg-white dark:bg-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]


  - block: contact-info
    id: contact
    content:
      title: Contact Us
      visit_title: Office
      connect_title: Contact Info
      address:
        lines:
          - Room 4118, N7-4, KAIST
          - 291 Daehak-ro, Yuseong-gu, Daejeon 34141
          - Republic of Korea

      email: jdltogether@gmail.com
      social:
        - icon: brands/linkedin
          url: https://www.linkedin.com/company/just-do-it-lab/
        - icon: brands/github
          url: https://github.com/jdltogether-netizen
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
