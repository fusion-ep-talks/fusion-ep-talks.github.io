---
title: "Plasma cleaning of diagnostic mirrors in ITER"
date: 2022-02-22
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/kunal_soni.png
speaker: "Kunal Soni"
affiliation: "University of Basel, Switzerland"
youtube_id: "P7vy5K7KEbk"

# ==============================================================================
# SLIDES CONFIGURATION:
# - With slides:    Uncomment the line below and set the local path or URL.
# - Without slides: Keep the line commented out (#) or delete it entirely.
# ==============================================================================
# slides_url: "/assets/slides/presentation.pdf"

author_profile: false
---

**Speaker:** {{ page.speaker }}  
**Position & Institution:** {{ page.affiliation }}  
**Date:** {{ page.date | date: "%B %d, %Y" }}  
{% if page.slides_url %}
**Slides:** [Download Presentation (PDF)]({{ page.slides_url | relative_url }}){: .btn .btn--info .btn--small target="_blank" rel="noopener noreferrer"}  
{% endif %}

<div style="clear: both; margin-top: 1.5rem;"></div>

{% if page.youtube_id %}
### Recording

{% include video id=page.youtube_id provider="youtube" %}

<p style="text-align: center; margin-top: 1.25rem; display: flex; justify-content: center; gap: 0.75rem; flex-wrap: wrap;">
  <a href="https://www.youtube.com/watch?v={{ page.youtube_id }}" target="_blank" rel="noopener noreferrer" class="btn btn--primary">
    <i class="fab fa-youtube"></i> Watch on YouTube
  </a>
  {% if page.slides_url %}
  <a href="{{ page.slides_url | relative_url }}" target="_blank" rel="noopener noreferrer" class="btn btn--inverse">
    <i class="fas fa-file-pdf"></i> Download Slides (PDF)
  </a>
  {% endif %}
</p>
{% endif %}

---

### Abstract
Nearly 40 optical diagnostic systems in ITER are equipped with metallic first mirrors (FMs) with the objective of directing the light from the fusion plasma towards the diagnostics through an optical labyrinth in order to prevent neutron leakage. However, the FMs being the initial elements in the optical diagnostics, would be subject to constant erosion from charge exchange neutrals as well as deposition of the first wall materials: beryllium (Be), tungsten (W) and their oxides, that would significantly degrade their optical properties. The FMs would hence require regular cleaning to restore their optical properties, currently foreseen to be achieved by an in-situ capacitively coupled radio-frequency (CCRF) plasma cleaning technique. In this contribution we discuss the plasma cleaning of such FMs in ITER relevant conditions.
