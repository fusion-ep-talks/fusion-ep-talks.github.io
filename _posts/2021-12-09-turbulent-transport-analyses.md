---
title: "Turbulent transport analyses"
date: 2021-12-09
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/neeraj_kumar.png
speaker: "Dr. Neeraj Kumar"
affiliation: "University of Colorado Boulder, US"
youtube_id: "GjiHkxolXKs"

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
One of the major goals of the ITER project is to demonstrate high fusion power gain in a tokamak. In ITER, metallic plasma-facing components are chosen for their low tritium retention and ability to sustain high heat loads. However, tokamaks operation with metallic plasma-facing components raises issues regarding the control of high-Z impurities since the accumulation of heavy impurities such as tungsten (Z=74) in the plasma core leads to significant radiation losses and deteriorates the energy confinement. Transport of tungsten (W) in the central part of ITER (r/a< 0.3), is expected to be determined by neoclassical and turbulent processes, which strongly depend on the main ion density, temperature, and rotation profiles. Thus, a reliable understanding of the dominant transport mechanisms in the central part is crucial to accurately predict W core accumulation. Previous studies mostly focused on the edge and core regions (r/a > 0.3) and the central part remains relatively unexplored so far. The aim of this work is to advance our understandings of the dominant transport mechanism in the central region (r/a < 0.3) of tokamak plasmas by first validating the available transport models that are applied to ITER with measurements in existing tokamak plasmas and then using these models to evaluate turbulent transport in ITER. The existing experimental JET high-beta MHD-free hybrid H-mode discharge #75225 has been selected to investigate the characteristics of core micro-instabilities and to test the quasi- linear approximation in the inner core by means of linear and non-linear gyro-kinetic simulations using the gyro-kinetic code GKW in the local approximation limit. These results are compared with the radial region, r/a> 0.3, where much of the work has already been done previously.
