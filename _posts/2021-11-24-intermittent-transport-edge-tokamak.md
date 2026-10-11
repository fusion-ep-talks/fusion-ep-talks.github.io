---
title: "Intermittent transport at the edge of tokamak plasmas"
date: 2021-11-24
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/nicolas_fedorczak.png
speaker: "Dr. Nicolas Fedorczak"
affiliation: "IRFM - CEA, France"
youtube_id: "TTezL87Ra5c"

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
At the boundary of tokamak or stellarators plasmas, transport across magnetic confinement is generally associated to the intermittent propagation of isolated filaments, or blobs, considered ruling plasma wall interaction. Experimental investigations generally focus on constructing averaged blob observables, like shape, amplitude and propagation speeds, because those quantities can be directly compared to theoretical predictions for isolated blobs. This was carried on a large dataset collected in the Tore Supra tokamak, featuring simple circular geometry, and revealed a sound agreement with predictions. Yet, moving from isolated blob models to macroscopic transport models does require statistical laws for blobs that do not exist yet. Another point of view was adopted: what about describing those blobs as an assembly of spatial wave packets parametrized by wave spectra? It turns out that theoretical models for isolated blob dynamics can be adapted to models predicting the time averaged amplitude and shape of density and potential spectra. Verification and validation of this new spectral filament model is detailed, with implications for plasma wall interaction in tokamak reactors.
