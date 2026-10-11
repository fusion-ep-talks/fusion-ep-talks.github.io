---
title: "Pellet dynamics in Stellarator TJ-ll"
date: 2021-09-30
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/daniel_medina.png
speaker: "Daniel Medina"
affiliation: "CIEMAT, Spain"
youtube_id: "If_QR28RZvI"

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
Currently, cryogenic pellet injection is the leading core fueling technique, since it allows deeper fuel penetrations than conventional gas puffing and does not introduce an energy source in the plasma core. Despite this, some involved mechanisms, particularly for stellarators, remain unclear. For instance, pellet deflections have been observed in both stellarators and tokamaks and several models have been developed to explain this process. In tokamaks, a radial acceleration is usually observed, but predictions tend to overestimate the experimental observations. In contrast, in stellarators the situation is more complex, since pellets are also deflected in the vertical direction. In this work, pellet acceleration experiments are carried out in on-axis electron cyclotron resonance heated hydrogen plasmas in the TJ-II stellarator. The three-dimensional pellet trajectory and the different components of the pellet acceleration, assumed to be constant, are studied using the TJ-II double-bundle fast camera system. This allows estimating the dependency of the different components of the pellet acceleration on the plasma current, electron density and temperature, as well as pellet mass and injection velocity. In addition to the above, experimental results are compared with predictions from the stellarator version of the HPI2 code, including pellet acceler- ation. This is done by using the 1st Principles and Semi-empirical models in HPI2, recently extended to stellarators.
