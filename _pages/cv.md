---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 4
description: Education, research experience, projects, technical skills, and selected honors.
_styles: |
  .cv-download { display: inline-flex; align-items: center; gap: .45rem; margin: .4rem 0 1.8rem; padding: .5rem .75rem; border: 1px solid var(--global-divider-color); border-radius: 5px; color: var(--global-text-color); text-decoration: none; }
  .cv-download:hover { color: var(--global-theme-color); border-color: var(--global-theme-color); text-decoration: none; }
  .cv-header { margin-bottom: 2.4rem; }
  .cv-header h2 { margin: 0 0 .25rem; font-size: 1.5rem; }
  .cv-header p { margin: .12rem 0; color: var(--global-text-color-light); }
  .cv-section { margin: 2.6rem 0; }
  .cv-section > h2 { margin: 0 0 .8rem; padding-bottom: .45rem; border-bottom: 1px solid var(--global-divider-color); font-size: 1.25rem; }
  .cv-entry { display: grid; grid-template-columns: 8.5rem minmax(0, 1fr); gap: 1.4rem; padding: 1rem 0; }
  .cv-date { color: var(--global-text-color-light); font-size: .88rem; }
  .cv-entry h3 { margin: 0; font-size: 1rem; }
  .cv-subtitle { margin: .15rem 0 .55rem; color: var(--global-text-color-light); font-size: .92rem; }
  .cv-entry ul { margin: .45rem 0 0; padding-left: 1.15rem; }
  .cv-entry li { margin-bottom: .35rem; }
  .cv-line { display: grid; grid-template-columns: 11rem minmax(0, 1fr); gap: 1rem; padding: .45rem 0; }
  .cv-line strong { font-weight: 600; }
  @media (max-width: 650px) { .cv-entry, .cv-line { grid-template-columns: 1fr; gap: .2rem; } }
---

{% assign cv = site.data.cv.cv %}

<a class="cv-download" href="{{ '/assets/pdf/Ruidong_Zhang_CV.pdf' | relative_url }}"><i class="fa-solid fa-file-pdf" aria-hidden="true"></i> Download PDF</a>

<div class="cv-header">
  <h2>{{ cv.name }}</h2>
  <p>{{ cv.headline }}</p>
  <p><a href="mailto:{{ cv.email }}">{{ cv.email }}</a> <span aria-hidden="true">·</span> {{ cv.location }}</p>
</div>

{% for item in cv.sections.Summary %}<p>{{ item }}</p>{% endfor %}

<section class="cv-section" aria-labelledby="cv-education">
  <h2 id="cv-education">Education</h2>
  {% for entry in cv.sections.Education %}
    <div class="cv-entry">
      <div class="cv-date">{{ entry.start_date | date: "%b. %Y" }} – {% if entry.end_date == "present" %}Present{% else %}{{ entry.end_date | date: "%b. %Y" }}{% endif %}</div>
      <div>
        <h3>{{ entry.institution }}</h3>
        <p class="cv-subtitle">{{ entry.degree }} in {{ entry.area }} · {{ entry.location }}</p>
        {% if entry.highlights %}<ul>{% for highlight in entry.highlights %}<li>{{ highlight }}</li>{% endfor %}</ul>{% endif %}
      </div>
    </div>
  {% endfor %}
</section>

<section class="cv-section" aria-labelledby="cv-research-experience">
  <h2 id="cv-research-experience">Research Experience</h2>
  {% for entry in cv.sections["Research Experience"] %}
    <div class="cv-entry">
      <div class="cv-date">{{ entry.start_date | date: "%b. %Y" }} – {{ entry.end_date | date: "%b. %Y" }}</div>
      <div>
        <h3>{{ entry.company }}</h3>
        <p class="cv-subtitle">{{ entry.position }} · {{ entry.location }}</p>
        <ul>{% for highlight in entry.highlights %}<li>{{ highlight }}</li>{% endfor %}</ul>
      </div>
    </div>
  {% endfor %}
</section>

<section class="cv-section" aria-labelledby="cv-industry-experience">
  <h2 id="cv-industry-experience">Industry Experience</h2>
  {% for entry in cv.sections["Industry Experience"] %}
    <div class="cv-entry">
      <div class="cv-date">{{ entry.start_date | date: "%b. %Y" }} – {{ entry.end_date | date: "%b. %Y" }}</div>
      <div>
        <h3>{{ entry.company }}</h3>
        <p class="cv-subtitle">{{ entry.position }} · {{ entry.location }}</p>
        <ul>{% for highlight in entry.highlights %}<li>{{ highlight }}</li>{% endfor %}</ul>
      </div>
    </div>
  {% endfor %}
</section>

<section class="cv-section" aria-labelledby="cv-projects">
  <h2 id="cv-projects">Projects</h2>
  {% for entry in cv.sections.Projects %}
    <div class="cv-entry">
      <div class="cv-date">
        {% if entry.start_date %}{{ entry.start_date | date: "%b. %Y" }} – {% if entry.end_date == "present" %}Present{% else %}{{ entry.end_date | date: "%b. %Y" }}{% endif %}{% endif %}
      </div>
      <div>
        <h3>{{ entry.name }}</h3>
        <p class="cv-subtitle">{{ entry.summary }}</p>
        {% if entry.highlights %}<ul>{% for highlight in entry.highlights %}<li>{{ highlight }}</li>{% endfor %}</ul>{% endif %}
      </div>
    </div>
  {% endfor %}
</section>

<section class="cv-section" aria-labelledby="cv-skills">
  <h2 id="cv-skills">Technical Skills</h2>
  {% for entry in cv.sections["Technical Skills"] %}<div class="cv-line"><strong>{{ entry.label }}</strong><span>{{ entry.details }}</span></div>{% endfor %}
</section>

<section class="cv-section" aria-labelledby="cv-honors">
  <h2 id="cv-honors">Awards</h2>
  <ul>{% for entry in cv.sections["Selected Honors"] %}<li>{{ entry.bullet }}</li>{% endfor %}</ul>
</section>
