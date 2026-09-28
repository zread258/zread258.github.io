---
layout: page
title: Home
permalink: /
description: Ruidong Zhang is an M.S. student at USTC working on compiler systems, GPU and AI systems, and hardware–software co-design.
nav: false
_styles: |
  .post-header { display: none; }
  .home-intro { display: grid; gap: 2.5rem; align-items: start; margin: 1.2rem 0 3rem; }
  .home-intro.has-photo { grid-template-columns: minmax(0, 1fr) 240px; }
  .home-photo { width: 240px; aspect-ratio: 4 / 5; object-fit: cover; border-radius: 8px; border: 1px solid var(--global-divider-color); }
  .home-name { margin: 0; font-size: clamp(2rem, 5vw, 2.65rem); line-height: 1.1; letter-spacing: -.025em; }
  .home-role { margin: .65rem 0 0; font-size: 1.08rem; font-weight: 500; }
  .home-affiliation { display: block; margin-top: .12rem; color: var(--global-text-color-light); font-size: 1rem; font-weight: 400; }
  .intro-copy { max-width: 73ch; margin-top: 1.45rem; }
  .intro-copy p { margin-bottom: .8rem; }
  .link-row { display: flex; flex-wrap: wrap; gap: .55rem; margin: 1.1rem 0 0; }
  .quiet-button { display: inline-flex; align-items: center; gap: .42rem; padding: .45rem .72rem; border: 1px solid var(--global-divider-color); border-radius: 5px; color: var(--global-text-color); text-decoration: none; font-size: .9rem; }
  .quiet-button:hover { border-color: var(--global-theme-color); color: var(--global-theme-color); text-decoration: none; }
  .quiet-button:focus-visible { outline: 3px solid var(--global-theme-color); outline-offset: 2px; }
  .home-section { margin: 2.75rem 0; }
  .section-heading { margin: 0 0 1rem; padding-bottom: .48rem; border-bottom: 1px solid var(--global-divider-color); font-size: 1.3rem; }
  .interest-grid { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 1.5rem; }
  .interest-item { padding-top: .7rem; border-top: 1px solid var(--global-theme-color); }
  .interest-item h3 { margin: 0 0 .35rem; font-size: 1rem; }
  .interest-item p { margin: 0; color: var(--global-text-color-light); font-size: .92rem; }
  .work-list { border-top: 1px solid var(--global-divider-color); }
  .work-row { display: grid; grid-template-columns: 15rem minmax(0, 1fr); gap: 1.25rem; padding: .82rem 0; border-bottom: 1px solid var(--global-divider-color); }
  .work-row p { margin: 0; }
  .work-org { font-weight: 600; }
  .work-meta { margin-top: .1rem; color: var(--global-text-color-light); font-size: .86rem; }
  .text-link { font-weight: 500; }
  .contact-line { padding-top: 1rem; border-top: 1px solid var(--global-divider-color); }
  .contact-line p { max-width: 74ch; margin-bottom: .45rem; }
  @media (max-width: 767px) {
    .home-intro.has-photo { grid-template-columns: 1fr; }
    .home-photo { width: min(220px, 62vw); order: -1; }
    .interest-grid { grid-template-columns: 1fr; gap: 1.1rem; }
    .work-row { grid-template-columns: 1fr; gap: .28rem; }
    .home-section { margin: 2.35rem 0; }
  }
---

<section class="home-intro{% if site.data.profile.profile_image != '' %} has-photo{% endif %}" aria-labelledby="ruidong-zhang">
  <div>
    <h1 class="home-name" id="ruidong-zhang">Ruidong Zhang</h1>
    <p class="home-role">M.S. Student in Computer Science <span class="home-affiliation">University of Science and Technology of China (USTC)</span></p>
    <div class="intro-copy">
      <p>I am an M.S. student at USTC working at the intersection of compilers and computer systems. My research focuses on compiler abstractions that preserve application structure and generate efficient code for heterogeneous hardware.</p>

      <p>My recent work spans MLIR/LLVM-based compilation, GPU performance analysis, multi-GPU AI inference, and processor design. Before joining USTC, I received my B.S. in Computer Science from UESTC.</p>
    </div>
    <div class="link-row" aria-label="Contact and profile links">
      <a class="quiet-button" href="mailto:zread258@gmail.com"><i class="fa-solid fa-envelope" aria-hidden="true"></i> Email</a>
      <a class="quiet-button" href="{{ '/assets/pdf/Ruidong_Zhang_CV.pdf' | relative_url }}"><i class="fa-solid fa-file-pdf" aria-hidden="true"></i> CV</a>
      {% if site.data.profile.github_url != '' %}<a class="quiet-button" href="{{ site.data.profile.github_url }}"><i class="fa-brands fa-github" aria-hidden="true"></i> GitHub</a>{% endif %}
      {% if site.data.profile.orcid_url != '' %}<a class="quiet-button" href="{{ site.data.profile.orcid_url }}"><i class="ai ai-orcid" aria-hidden="true"></i> ORCID</a>{% endif %}
      {% if site.data.profile.scholar_url != '' %}<a class="quiet-button" href="{{ site.data.profile.scholar_url }}"><i class="ai ai-google-scholar" aria-hidden="true"></i> Scholar</a>{% endif %}
    </div>

  </div>
  {% if site.data.profile.profile_image != '' %}
    <img class="home-photo" src="{{ site.data.profile.profile_image | prepend: '/assets/img/' | relative_url }}" alt="Ruidong Zhang" width="240" height="300" loading="eager">
  {% endif %}
</section>

<section class="home-section" aria-labelledby="research-focus">
  <h2 class="section-heading" id="research-focus">Research Interests</h2>
  <div class="interest-grid">
    <div class="interest-item">
      <h3>Compiler Systems</h3>
      <p>MLIR/LLVM, IR design, domain-specific compilation, structured transformation, and target-aware code generation.</p>
    </div>
    <div class="interest-item">
      <h3>GPU &amp; AI Systems</h3>
      <p>CUDA execution, memory hierarchy, kernel profiling, heterogeneous computing, and multi-GPU inference.</p>
    </div>
    <div class="interest-item">
      <h3>Architecture &amp; Co-design</h3>
      <p>RISC-V, FPGA prototyping, accelerators, and compiler support for heterogeneous hardware.</p>
    </div>
  </div>
</section>

<section class="home-section" aria-labelledby="selected-experience">
  <h2 class="section-heading" id="selected-experience">Selected Work</h2>
  <div class="work-list">
    <div class="work-row"><div><div class="work-org">Shanghai AI Laboratory</div><div class="work-meta">Research Intern · High-Performance Compilation · 2026</div></div><p>MLIR-based compiler infrastructure, transformations, lowering, GPU code generation, and performance analysis. One manuscript from this work is currently under double-blind review.</p></div>
    <div class="work-row"><div><div class="work-org">Ubiquant Technology</div><div class="work-meta">Quantitative Implementation Intern · 2026</div></div><p>Multi-node, multi-GPU LLM inference and profiling of compute, memory, and communication bottlenecks.</p></div>
    <div class="work-row"><div><div class="work-org">Houmo Technology</div><div class="work-meta">AI Compiler Development Intern · 2025</div></div><p>Implemented 44 ONNX operators through MLIR rewriting and hardware-specific backend lowering.</p></div>
  </div>
  <p><a class="text-link" href="{{ '/experience/' | relative_url }}">Full experience</a></p>
</section>

<section class="home-section contact-line" aria-labelledby="contact">
  <h2 class="section-heading" id="contact">Contact</h2>
  <p>For research discussions or collaboration opportunities, contact me at <a href="mailto:zread258@gmail.com">zread258@gmail.com</a>.</p>
  {% if site.data.profile.internship_availability %}<p>I am currently interested in research internship opportunities in compiler and computer systems.</p>{% endif %}
</section>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Ruidong Zhang",
  "url": "{{ site.url }}{{ site.baseurl }}/",
  "email": "mailto:zread258@gmail.com",
  "jobTitle": "M.S. Student in Computer Science",
  "affiliation": {
    "@type": "CollegeOrUniversity",
    "name": "University of Science and Technology of China"
  }
}
</script>
