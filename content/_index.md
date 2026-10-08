sections:
  - block: hero
    id: about
    content:
      title: |
        <a href="https://me.kaist.ac.kr/" target="_blank" rel="noopener" title="KAIST Department of Mechanical Engineering" style="display:block;width:max-content;margin:0 auto 1.5rem"><img src="media/me-logo.png" alt="KAIST Department of Mechanical Engineering" style="display:block;height:4rem;width:auto" /></a>
        <span style="display:block;font-size:0.5em;line-height:1.2;letter-spacing:0.01em;color:var(--color-primary-500);margin-bottom:1.75rem">Just Do it Lab</span>
        <span style="display:block">Convergence Technology: From Rigorous Research to Real Ventures</span>
      text: |
        JDL is an Open Lab at KAIST Mechanical Engineering for convergence technology and commercialization, spanning additive manufacturing, semiconductor convergence processes, and AI-driven autonomous drone production.
      primary_action:
        text: Explore Our Research
        url: 'research/'
        icon: hero/beaker
      secondary_action:
        text: View Publications
        url: 'publications/'
        icon: hero/academic-cap
      announcement:
        text: "Now hiring PhD students, Master’s students, and postdocs!"
        link:
          text: "Apply now"
          url: "opportunities/"
    design:
      css_class: ""
      background:
        gradient_mesh:
          enable: true
          style: "waves"
          animation: "pulse"
          intensity: "medium"
          colors:
            - "primary-500/30"
            - "blue-600/20"
            - "indigo-600/15"

  - block: cta-image-paragraph
    content:
      items:
        - title: 'State-of-the-Art Research Environment'
          text: |
            JDL runs its own fabrication, characterization, and compute rather than queuing for shared facilities. Students design, print, process, and measure in house across KAIST, KPU, and NTU's Singapore Centre for 3D Printing.
          image: facilities/kpu-08-yellow-room.jpg
          feature_icon: hero/check-circle
          features:
            - 'Additive Manufacturing: DLP and FDM printers, in-house filament fabrication, UV curing, two-photon polymerization'
            - 'Thin-Film & Semiconductor: ALD, PLD, sputtering, e-beam evaporation, PECVD, deep reactive ion etching, yellow room'
            - 'Characterization: confocal microscopy, SEM, X-ray diffraction, impedance spectroscopy, tensile testing'
            - 'AI Computing: RTX 5090 nodes, RTX A-series workstations, NAS storage'
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
            - 'On-demand, distributed drone production'

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
            JDL is small enough that everyone knows what everyone else is building. Postdocs and senior students support newer members, and the group meets, eats, and gets out of the building together.
          image: current-members/group-hero.jpg
          feature_icon: hero/heart
          features:
            - 'Mechanical engineering, computer science, electrical engineering, and materials work side by side'
            - 'An open door: ask, and you get time on your problem'
            - 'Biweekly Friday group meetings and lab outings'
    design:
      css_class: "bg-white dark:bg-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]

  - block: contact-info
    id: contact
    content:
      title: Contact
      subtitle: ''
      text: ''
      coordinates:
        latitude: 36.3725
        longitude: 127.3604
      address:
        street: Department of Mechanical Engineering
        city: KAIST
        region: Daejeon
        postcode: "34141"
        country: Republic of Korea
      email: yjyoon@kaist.ac.kr
      phone: ""
      appointment_url: ""
      directions: ''
      office_hours: ''
    design:
      css_class: "bg-gray-50 dark:bg-gray-900"
      spacing:
        padding: ["4rem", 0, "4rem", 0]
---
