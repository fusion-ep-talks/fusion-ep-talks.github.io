---
title: "High-Temperature superconducting magnets"
date: 2021-04-07
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/erica_salazar.png
speaker: "Erica Salazar"
affiliation: "MIT, US"
youtube_id: "xJ2h3vbOag4"

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
High temperature superconductors (HTS) have the ability to revolutionize the fusion energy industry by enabling tokamak fusion devices, such as the SPARC fusion device, to be smaller, lower cost, and faster to build. All fusion-class devices built to date have used either low temperature superconductors (LTS) or copper to generate magnetic fields to control and drive the plasma in a fusion device. In contrast to LTS, HTS magnets can withstand and generate significantly higher magnetic fields--leading to smaller and lower cost tokamak devices. However, introducing a new HTS material will bring new scientific challenges and risks. This presentation will highlight the risk reduction strategies and test results of the VIPER cable (a HTS cable designed by MIT and Commonwealth Fusion Systems) such as fabrication feasibility testing, load cycling, strain testing, and quench testing in SPARC-relevant conditions.
