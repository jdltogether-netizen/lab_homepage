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
        <img src="media/me-logo.png" alt="KAIST Department of Mechanical Engineering" style="display:block;height:4rem;width:auto;margin:0 auto 1.5rem" />
        <span style="display:block">Just Do it Lab</span>
      text: |
        of Additive Manufacturing & Semiconductor Convergence Process
      # Three distinct destinations in the hero: the announcement above
      # already sends people to /opportunities, so this button points at the
      # research instead of repeating it. Swap back to "Join Our Team" ->
      # /opportunities if recruiting should lead.
      primary_action:
        text: Research
        url: 'research/'
        icon: hero/beaker
      secondary_action:
        text: Publications
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
      items:

        # 1. Additive Manufacturing
        - title: 'Additive Manufacturing'
          text: |
            From FDM to DLP...
          image: research/Additive Manufacturing.png
          feature_icon: hero/check-circle
          features:
            - 'Additive Manufacturing: DLP and FDM printers, in-house filament fabrication, UV curing, two-photon polymerization'
            - 'Thin-Film & Semiconductor: ALD, PLD, sputtering, e-beam evaporation, PECVD, deep reactive ion etching, yellow room'
            - 'Characterization: confocal microscopy, SEM, X-ray diffraction, impedance spectroscopy, tensile testing'
            - 'AI Computing: RTX 5090 nodes, RTX A-series workstations, NAS storage, National AI Computing Center capacity'


        # 2. Artificial Intelligence
        - title: 'Artificial Intelligence'
          text: |
            recall AI
          image: research/Artificial Intelligence.png
          feature_icon: hero/users
          features:
            - '23 sponsors across government, industry, and overseas agencies'
            - 'A network spanning KAIST and NTU Singapore, with KRISS, KIMM, and ETRI'
            - 'A Global Start-up Platform that carries student projects into ventures'

        # 3. MAVs
        - title: 'MAVs'
          text: |
            Micro Aerial Vehicle
          image: research/SmallUAVs.png
          feature_icon: hero/heart
          features:
            - 'Help across disciplines: mechanical engineering, computer science, electrical engineering, and materials sit side by side'
            - 'An open door: ask, and you get time on your problem'
            - 'Biweekly Friday group meetings, and lab outings through the year'

        # 4. From Lab Bench to Production Line
        - title: 'From Lab Bench to Production Line'
          text: |
            The drone work now has a company behind it. [KEONIX Labs](https://keonix.co.kr), a KAIST faculty start-up, is taking the lab's manufacturing research into real production.
          image: research/drone-2d-to-3d.jpg
          feature_icon: hero/rocket-launch
          features:
            - 'Pocheon Center: a civil-military-government site for drone education and production'
            - 'Printers, training programs, and custom FPV drone builds'
            - 'With Chung-Ang, Jeonbuk National and Incheon National faculty, and KAIST InnoCORE PRISM-AI'
    
        # 5. Our Partners
        - title: 'Our Global Partners'
          text: |
    
          image: research/Partners.png
    
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
