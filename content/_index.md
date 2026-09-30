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
      title: |
        Just Do It Lab | AI division
        **AI-Driven Next-Gen Manufacturing & Drone Production**
      text: |
        We are a newly established AI division within the Just Do It Lab (JDL) at KAIST Mechanical Engineering, focused on AI-driven manufacturing and drone production technologies. Our multidisciplinary team develops intelligent production systems and actively translates research into real-world ventures, collaborating with regional governments and global collaborators.
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
      items:
        - statistic: "50+"
          description: Publications in top venues over the past 5 years
          sub_metric: Journals & Conferences in Mechanical Engineering & Computer Science.
          icon: hero/document-text
        - statistic: "7"
          description: Multidisciplinary researchers and scientists
          sub_metric: From mechanical engineering to computational science, electrical engineering, and design engineering
          icon: hero/user-group
        - statistic: "$1.5M"
          description: Active research & business funding
          sub_metric: Startup, KEONIX (founded by Prof. Yongjin Yoon & Dr. Hyeongcheol Kim) | C&Tech, TIPS, Pocheon-si, InnoCORE KAIST, Jeonbuk Physical AI Initiative, etc.
          icon: hero/currency-dollar
        - statistic: "2"
          description: Ongoing and newly secured projects, with parallel startup initiatives
          sub_metric: InnoCORE PRISM-AI, Jeonbuk Physical AI Initiative, KEONIX with Pocheon
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
      text: Our research integrates artificial intelligence, advanced manufacturing, and autonomous systems to transform how complex products are designed, optimized, and produced in real-world environments.
      items:
        - name: AI-Enhanced Additive Manufacturing
          description: Developing intelligent additive manufacturing systems that monitor, analyze, and optimize fabrication processes in real time using multimodal sensor data, machine learning, and adaptive control.
          icon: hero/cube-transparent
          gradient: from-green-400 to-emerald-600
          status: active
          topics:
            - Real-Time Process Monitoring
            - Sensor Fusion
            - Predictive Quality Control
            - Inverse Material Design
          team_size: 2
          publications: 5+
          funding: $0.5M Government/Industry
          cta:
            text: Explore Projects
            url: /research/computational-biology
            
        - name: LLM Agents for Industrial Intelligence
          description: Building large language model-based autonomous agents that capture expert tacit knowledge, transform operational know-how into machine-readable workflows, and automate engineering decision-making.
          icon: hero/command-line
          gradient: from-blue-400 to-indigo-600
          status: active
          topics:
            - Industrial LLM Agents
            - Workflow Automation
            - Knowledge Extraction
            - Graph Neural Networks
            - Multimodal Reasoning
            - Human-AI Collaboration
          team_size: 2
          publications: 2+
          funding: $0.2M Industry
          cta:
            text: View Research
            url: /research/machine-learning
            
        - name: Physical AI for Autonomous Production
          description: Advancing physical AI systems that combine generative design, virtual simulation, robotics, and additive manufacturing to enable flexible and autonomous production of next-generation drone systems.
          icon: hero/rocket-launch
          gradient: from-purple-400 to-pink-600
          status: emerging
          topics:
            - Generative Design
            - Simulation-to-Reality
            - Robotic Production
            - Autonomous Drone Production
          team_size: 3
          publications: 2+
          funding: $1.2M Venture Capital
          cta:
            text: Learn More
            url: /research/materials-science
      cta:
        text: Active Research Projects
        url: /#research
        icon: hero/arrow-right
    design:
      layout: cards
      css_class: "bg-gradient-to-b from-gray-50 to-white dark:from-gray-900 dark:to-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]

  - block: cta-image-paragraph
    content:
      items:
        - title: 'State-of-the-Art Research Environment'
          text: |
             To establish a world-class AI-driven manufacturing environment, our laboratory is expanding next-generation computational infrastructure. We are acquiring AI workstations equipped with NVIDIA GeForce RTX 5060 (Blackwell) and RTX A6000 GPUs for large-scale AI training, simulation, and digital manufacturing research. These systems will integrate with high-capacity NAS storage to support scalable research data and digital twin workflows.
          image: pexels-polina-tankilevitch-3735769.jpg
          feature_icon: hero/check-circle
          features:
             - 'High-Performance AI Workstations: NVIDIA RTX 5060 (Blackwell) and RTX A6000 computing nodes for AI training and simulation'
             - 'Scalable Research Storage: Enterprise NAS systems for large-scale multimodal data and digital twin workflows'
             - 'Autonomous Experimental Platforms: Robotic arms, additive manufacturing systems, and embedded sensing infrastructure'
          button:
            text: 'Virtual Lab Tour'
            url: '/facilities'

        - title: 'Collaborative Innovation Culture' 
          text: |
            Our team brings together experts in AI, robotics, electronics, design engineering, industrial automation, and additive manufacturing. With researchers trained at leading universities worldwide, we maintain a strong global research network. Through close collaboration with industry and deep-tech startups, we accelerate real-world innovation, where both Korean and English enable seamless technical communication across diverse teams.
          image: pexels-canvastudio-3153198.jpg
          feature_icon: hero/users
          features:
             - 'Multidisciplinary Expertise: AI, robotics, electronics, manufacturing, and design engineering'
             - 'Global Research Network: International faculty and alumni connections across leading universities'
             - 'Industry & Startup Collaboration: Technology transfer, commercialization, and global English-based collaboration'
          button:
            text: 'Join Our Community'
            url: '/opportunities'
    design:
      css_class: "bg-white dark:bg-gray-800"
      spacing:
        padding: ["0rem", 0, "0rem", 0]

  - block: team-showcase
    id: team
    content:
      title: Meet Our Team
      subtitle: 'World-class researchers pushing the boundaries of science & engineering technologies'
      text: 'Our multidisciplinary team pioneers technologies and innovations that accelerate AI-driven manufacturing automation and advance next-gen on-site drone production.'
      user_groups:
        - Principal Investigators
        - Postdoctoral Researchers
        - PhD Students
        - Master Students
        - Interns
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

  - block: collection
    id: projects
    content:
      title: Active Research Projects
      subtitle: ''
      text: ''
      filters:
        folders:
          - projects
      count: 0  # Number of items to show (0 = all)
      # Default filter UI (for future release)
      #default_button_index: 0
      # Filter toolbar (optional)
      # Add or remove as many filters as you like
    #   buttons:
    #     - name: All
    #       tag: '*'
    #     - name: Machine Learning
    #       tag: ML
    #     - name: Biology
    #       tag: Biology
    #     - name: Materials
    #       tag: Materials
    design:
      view: article-grid
      columns: 2
      spacing:
        padding: ["5rem", 0, "0rem", 0]

  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
      count: 5
    design:
      view: citation
      spacing:
        padding: ["3rem", 0, "0rem", 0]

  - block: collection
    id: featured
    content:
      title: Featured Research
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
      spacing:
        padding: ["5rem", 0, "0rem", 0]

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
        - icon: brands/jdl
          url: https://jdl.kaist.ac.kr
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