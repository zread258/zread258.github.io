---
# Display name
title: Ruidong Zhang

# Name pronunciation (optional)
# name_pronunciation: Chien Shiung Wu

# Full name (for SEO)
first_name: Ruidong
last_name: Zhang

# Status emoji
status:
  icon: ☕️

# Is this the primary user of the site?
superuser: true

# Highlight the author in author lists? (true/false)
highlight_name: true

# Role/position/tagline
role: Master of Computer Science

# Organizations/Affiliations to display in Biography blox
organizations:
  - name: University of Science and Technology of China
    url: https://www.ustc.edu/

# Social network links
# Need to use another icon? Simply download the SVG icon to your `assets/media/icons/` folder.
profiles:
  - icon: at-symbol
    url: 'mailto:zread258@gmail.com'
    label: E-mail Me
  # - icon: brands/x
  #   url: https://twitter.com/GetResearchDev
  # - icon: brands/instagram
  #   url: https://www.instagram.com/
  - icon: brands/github
    url: https://github.com/zread258
  # - icon: brands/linkedin
  #   url: https://www.linkedin.com/
  # - icon: academicons/google-scholar
  #   url: https://scholar.google.com/
  # - icon: academicons/orcid
  #   url: https://orcid.org/

interests:
  - Computer Architecture
  - AI Complier

education:
  - area: Master in Computer Science
    institution: University of Science and Technology of China
    date_start: 2025-09-09
    date_end: 2028-06-30
  - area: BSc in Computer Science
    institution: University of Electronic Science and Technology of China
    date_start: 2021-08-26
    date_end: 2025-06-30
    summary: |
      GPA: 3.84/4.0
work:
  - position: AI Complier Develop Intern
    company_name: Beijing Houmo Technology Co.
    company_url: 'www.houmoai.com'
    company_logo: ''
    date_start: 2025-04-07
    date_end: '2025-07-18'
    summary: |2-
      Deeply involved in the development and optimization of core modules for a neural network compiler targeting proprietary AI accelerators, with a focus on expanding model coverage, enhancing performance, and ensuring stability.

      Key Achievements & Responsibilities:
      - Operator Library Expansion: Led the end-to-end implementation of 44 standard ONNX operators, spanning the entire stack from frontend MLIR dialect definition and mid-level pattern rewriting to backend hardware-specific primitive implementation. This work substantially broadened the compiler's capabilities, enabling support for advanced models like Vision Transformer (ViT).

      - Low-Level Hardware Primitive Development: Developed and optimized low-level operator primitives for custom AI hardware featuring RISC-V Vector (RVV) extensions. I independently authored vectorized (RVV) implementations for bitwise binary operators, introduced foundational support for new data types (e.g., uint), and implemented safety mechanisms to prevent undefined behavior in bit-shift operations.

      - Compiler Architecture & Optimization Strategy: Leveraged MLIR's declarative pattern rewriting framework to efficiently decompose complex operators (e.g., PReLU, Sign) into a combination of simpler, hardware-friendly primitives, improving compiler modularity and extensibility. Furthermore, I architected and integrated a new PostFrontend compilation stage, laying the groundwork for advanced graph-level optimizations like operator fusion.

      - Automated Testing & Validation Framework: Designed and implemented a comprehensive automated testing and validation framework. This included developing scripts to auto-generate single-operator test cases and establishing a golden-generation pipeline using ONNX Runtime for standard models. This two-tiered system ensures both operator-level and model-level correctness, guaranteeing the integrity of the compiler through continuous development.

# Skills
# Add your own SVG icons to `assets/media/icons/`
skills:
  - name: Technical Skills
    items:
      - name: Python
        description: ''
        percent: 80
        icon: code-bracket
      - name: Data Science
        description: ''
        percent: 100
        icon: chart-bar
      - name: SQL
        description: ''
        percent: 40
        icon: circle-stack
  - name: Hobbies
    color: '#eeac02'
    color_border: '#f0bf23'
    items:
      - name: Hiking
        description: ''
        percent: 60
        icon: person-simple-walk
      - name: Cats
        description: ''
        percent: 100
        icon: cat
      - name: Photography
        description: ''
        percent: 80
        icon: camera

# Awards.
#   Add/remove as many awards below as you like.
#   Only `title`, `awarder`, and `date` are required.
#   Begin multi-line `summary` with YAML's `|` or `|2-` multi-line prefix and indent 2 spaces below.
awards:
  - title: Neural Networks and Deep Learning
    url: https://www.coursera.org/learn/neural-networks-deep-learning
    date: '2023-11-25'
    awarder: Coursera
    icon: coursera
    summary: |
      I studied the foundational concept of neural networks and deep learning. By the end, I was familiar with the significant technological trends driving the rise of deep learning; build, train, and apply fully connected deep neural networks; implement efficient (vectorized) neural networks; identify key parameters in a neural network’s architecture; and apply deep learning to your own applications.
  - title: Blockchain Fundamentals
    url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
    date: '2023-07-01'
    awarder: edX
    icon: edx
    summary: |
      Learned:
      - Synthesize your own blockchain solutions
      - Gain an in-depth understanding of the specific mechanics of Bitcoin
      - Understand Bitcoin’s real-life applications and learn how to attack and destroy Bitcoin, Ethereum, smart contracts and Dapps, and alternatives to Bitcoin’s Proof-of-Work consensus algorithm
  - title: 'Object-Oriented Programming in R'
    url: https://www.datacamp.com/courses/object-oriented-programming-with-s3-and-r6-in-r
    certificate_url: https://www.datacamp.com
    date: '2023-01-21'
    awarder: datacamp
    icon: datacamp
    summary: |
      Object-oriented programming (OOP) lets you specify relationships between functions and the objects that they can act on, helping you manage complexity in your code. This is an intermediate level course, providing an introduction to OOP, using the S3 and R6 systems. S3 is a great day-to-day R programming tool that simplifies some of the functions that you write. R6 is especially useful for industry-specific analyses, working with web APIs, and building GUIs.
---

## About Me

I am a 1st-year master student in computer science driven by a passion for building efficient computing platforms. My interest spans both Computer Architecture and AI Compiler, with a core focus on unlocking performance through hardware-software co-design.
