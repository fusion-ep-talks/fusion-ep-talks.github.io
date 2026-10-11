---
title: "Lower hybrid current drive"
date: 2021-07-22
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/daniela_teplova.png
speaker: "Daniela Teplova"
affiliation: "ITMO University, Peter the Great St. Petersburg Polytechnic University, Russia"
youtube_id: "S7l0qn8h_mI"

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
Experimentally approved and validated methods of current generation in a tokamak are injection of neutral beams and using electromagnetic waves. At present, the method of generating current by means of slowed-down high-frequency waves of the lower hybrid (LH) frequency range (Δf ≈ (1-10) GHz) is widely used in traditional type tokamaks (with an aspect ratio of R / a> 2) and has the highest theoretically and experimentally confirmed efficiency. The method is based on the effect of the transmission of a pulse by a slowed-down RF wave in the lower hybrid frequency range to electrons due to Landau damping. As a result, the electron distribution function (EDF) is deformed, which ensures an increase in the total current in the tokamak plasma. This method is still considered as a candidate for the current generation in ITER. In an experiment the loop voltage drop is measured and associated to the level of current drive. As soon as direct measurements of the LH current are not possible the numerical model predicting the level of the LH current and its radial distribution is required. Natalia Teplova will give an insight to physical basics of the lower hybrid current drive in tokamaks, describe the numerical models and show the examples of modeling for tokamaks of traditional type and spherical tokamak Globus-M2.
