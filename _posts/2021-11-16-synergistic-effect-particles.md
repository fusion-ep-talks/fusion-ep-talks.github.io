---
title: "Synergistic effects of particle and transient heat loads on ITER-grade tungsten"
date: 2021-11-16
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/mauricio_gago.png
speaker: "Dr. Mauricio Gago"
affiliation: "Forschungszentrum Jülich, Germany"
youtube_id: "d1JTYbAA9iQ"

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
Once ITER commences full power operation, the ITER divertor will be exposed to high thermal and particle loads. Tungsten was chosen as plasma facing material for the ITER divertor. It is, therefore, of the utmost importance to understand the behavior of ITER-grade tungsten under conditions similar to those it will have to withstand inside the reactor. To achieve this, ITER-grade tungsten samples were studied in the linear plasma device PSI-2, simulating the conditions expected in the ITER divertor by exposing them to a stationary D/He(6%) plasma and transient heat loads to simulate the effect of transient events such as edge-localized modes (ELMs).
