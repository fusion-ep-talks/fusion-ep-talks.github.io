---
title: "Integrated modelling of impurity transport on WEST"
date: 2021-10-07
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/david_sosa.png
speaker: "Dr. David Sosa"
affiliation: "IRFM - CEA, France"
youtube_id: "zwMv9Ss9PMQ"

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
The development and validation of integrated modelling tools that can be applied to the initial current ramp-up phase in Tokamaks is necessary to design a suitable current ramp for fusion scenarios, that lead to peaked and current density profiles, maximizing core heating and current diffusion in order to avoid radiative collapse and MHD instabilities. Since a good understanding of current diffusion physics is needed, in this work we first develop a simple current diffusion model to highlight how different parameters affect this process. Then we solve the complete resistive current diffusion equation using METIS to estimate the changes in the effective charge, Zeff , induced experimentally by Nitrogen seeding in plasmas of the WEST Tokamak. This study indicates that the increment is only weakely dependent on the Nitrogen puffing rate and suggests that the profile is slightly peaked. Transport analysis is then performed using QuaLiKiz to explore more in detail how Nitrogen affects turbulent transport and micro-stability. It is found that Nitrogen injection enhances TEM modes and stabilises ETG near the plasma edge and increases the particle and electron heat fluxes.
