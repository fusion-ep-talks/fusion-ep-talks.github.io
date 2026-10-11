---
title: "The ZPIC educational code suite"
date: 2021-09-14
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/ricardo_fonseca.png
speaker: "Prof. Dr. Ricardo Fonseca"
affiliation: "University Institute of Lisbon, Portugal"
youtube_id: "W5vMwLHdefc"

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
Particle-in-Cell (PIC) codes are used in almost all areas of plasma physics, such as fusion energy research, plasma accelerators, space physics, ion propulsion, and plasma processing, and many other areas. The ZPIC educational code suite, that we develop, intents to foster training in plasma physics using computer simulations by providing an easy to install and use framework, that students and researchers can use not only to learn about PIC simulations, but also to explore both textbook and advanced plasma physics scenarios, and to reproduce published results. ZPIC can be used interactively using Jupiter (Python) notebooks, and we have developed a set of well documented notebooks, with example problems of textbook and advanced plasma mechanisms, ranging from Debye shielding, to EM waves in density ramps and kinetic instabilities, that also include instructions for parameter space exploration. Additionally, we also prepared notebooks that reproduce and extend the work done in seminal plasma physics papers, such as the “Laser Electron Accelerator”, also allowing for parameter exploration. In this talk I will give a brief overview of the PIC algorithm and the ZPIC code suite, and I will demonstrate the use of ZPIC to model kinetic plasma scenarios.
