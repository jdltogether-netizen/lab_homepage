---
title: Research
type: landing
summary: What the lab does, and the research media behind it.

# The three focus areas also appear on the homepage as a summary. Keep the
# two in step: this page is the full version, the homepage is the teaser.
sections:
  - block: markdown
    content:
      title: About Us
      text: |
        ### Additive Manufacturing
        - 3D/4D Printing
        - Process Optimization
        - AI-based Prediction & Control

        ### Dynamic Systems & UAVs
        - Lightweight Structures
        - Mechanism Design
        - Dynamic Analysis & Simulation

        ### Design & Optimization
        - Structural Optimization
        - Vibration & Shock Control

        <img src="/media/research/main%20research.png" alt="JDL Research Areas" style="width:100%;height:auto;border-radius:.5rem" />
    design:
      spacing:
        padding: ["3rem", 0, "1rem", 0]
    
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


  - block: research-areas
    content:
      title: Research Focus Areas
      subtitle: Pioneering AI-Driven Next-Generation Manufacturing
      text: Our research integrates artificial intelligence, advanced additive manufacturing, and autonomous systems to transform how complex products are designed, optimized, and produced in real-world environments.
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
    design:
      layout: cards
      css_class: "bg-gradient-to-b from-gray-50 to-white dark:from-gray-900 dark:to-gray-800"
      spacing:
        padding: ["1rem", 0, "1rem", 0]

  - block: markdown
    content:
      title: Research Media
      text: |
        ### Future of the drone manufacturing: 2D sheet to 3D structure

        <div style="position:relative;padding-top:56.25%;margin:0 0 1rem"><iframe src="https://www.youtube.com/embed/62wto-q1W1c" title="Future of the drone manufacturing: 2D sheet to 3D structure" loading="lazy" allowfullscreen style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:.5rem"></iframe></div>

        This conceptual video, titled "Future of the drone manufacturing: 2D sheet to 3D structure," visualizes our core research philosophy of achieving rapid and robust manufacturing. To enable on-demand, decentralized production regardless of location, we are integrating 3D printing technology with folding-inspired deployable architectures. By rapidly printing a planar 2D sheet that systematically expands into a functional 3D aerodynamic structure, we aim to pioneer a highly efficient and scalable manufacturing paradigm for next-generation drones. (*This conceptual video was generated by AI)

        ### Stereolithography Apparatus(SLA)-printed Shape Memory Polymers(SMPs) with complex geometries that recover within 11s upon thermal heating using hot water

        <div style="position:relative;padding-top:56.25%;margin:0 0 1rem"><iframe src="https://www.youtube.com/embed/TWMBFuwBVuQ" title="SLA-printed Shape Memory Polymers demonstration 1" loading="lazy" allowfullscreen style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:.5rem"></iframe></div>
        <div style="position:relative;padding-top:56.25%;margin:0 0 1rem"><iframe src="https://www.youtube.com/embed/VM5K6DcXoao" title="SLA-printed Shape Memory Polymers demonstration 2" loading="lazy" allowfullscreen style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:.5rem"></iframe></div>
        <div style="position:relative;padding-top:56.25%;margin:0 0 1rem"><iframe src="https://www.youtube.com/embed/ZK2_ip6DOXo" title="SLA-printed Shape Memory Polymers demonstration 3" loading="lazy" allowfullscreen style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:.5rem"></iframe></div>
        <div style="position:relative;padding-top:56.25%;margin:0 0 1rem"><iframe src="https://www.youtube.com/embed/zRxInNX67IA" title="SLA-printed Shape Memory Polymers demonstration 4" loading="lazy" allowfullscreen style="position:absolute;inset:0;width:100%;height:100%;border:0;border-radius:.5rem"></iframe></div>

        Reference: Choong, Y. Y. C., Maleksaeedi, S., Eng, H., Wei, J., & Su, P. C. (2017). 4D printing of high performance shape memory polymer using stereolithography. Materials & Design, 126, 219-225.
    design:
      spacing:
        padding: ["2rem", 0, "3rem", 0]
---
