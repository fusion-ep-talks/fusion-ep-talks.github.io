---
title: "Laser-Induced Breakdown Spectroscopy"
date: 2021-10-14
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/vishal_dwivedi.png
speaker: "Dr. Vishal Dwivedi"
affiliation: "Comenius University, Slovakia"
youtube_id: "1bcOGXqA9Wg"

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
In view of the safe and successful operation of future fusion devices, it is highly important to determine the quantity of retained fuel in the plasma-facing components (PFCs). Also, the choice of plasma-facing materials (PFMs) is a major concern. Owing to its advantages, i.e., in-situ analysis, online monitoring, and fast analysis, etc. Laser-Induced Breakdown Spectroscopy (LIBS) has been found the most promising analytical technique among the few already established techniques, for the quantitative and depth profile study of PFMs, and is being considered to be installed in international thermonuclear experimental reactor (ITER) in the form of a robotic arm. Our research group is dedicated to the study and detailed investigation of fusion-relevant (FR) PFMs using calibration-free LIBS (CF-LIBS). The talk will highlight a short description of the CF-LIBS technique, following some of the key results obtained from the study of FR materials and coatings using ns/ps CF-LIBS.
