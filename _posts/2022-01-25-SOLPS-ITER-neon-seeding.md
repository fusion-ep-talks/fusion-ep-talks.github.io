---
title: "SOLPS-ITER studies of neon seeding in EAST"
date: 2022-01-25
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/dieter_boayaert.png
speaker: "Dr. Bieter Boeyaert"
affiliation: "University of Wisconsin, US"
youtube_id: "qpKPILXDwv4"

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
In order to decrease power and particle loads towards the divertor targets in future fusion devices, active extrinsic impurity seeding is required [1]. A dedicated experimental program on neon seeding in H-mode plasmas was performed at EAST [2]. Experimental observations show a factor of three reduction of the power flux towards the targets, but this is not sufficient to determine whether detachment is reached. Therefore, the SOLPS-ITER code package [3] is employed for assessing the plasma edge transport in the EAST discharges of ref. [2]. Drift terms are successfully included, resulting in upstream agreement within the experimental error bars and downstream agreement within a factor three or better between simulations and experiments, and showing that Ne seeding induces detachment. Sensitivity studies towards the main unknown input parameters for the code are executed. In order to quantify the precision of the performed simulations, the numerical errors affecting the simulation results are examined. Similar to previous ITER simulations with B2-EIRENE [4], the main error is the discretization error due to the finite plasma grid. By making an appropriate choice of the remaining numerical input parameters, the error contributions induced by the Monte Carlo noise of the EIRENE code are kept sufficiently small. [1] M. Wischmeier et al., J. Nucl. Mater. 463 (2015) 22-29 [2] D. Boeyaert et al., Nucl. Mater. Energy 26 (2021) 100926 [3] S. Wiesen et al., J. Nucl. Mater. 463 (2015) 480-484 [4] K. Ghoos et al., Nucl. Fusion 59 (2018) 026001
