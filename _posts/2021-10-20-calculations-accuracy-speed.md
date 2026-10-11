---
title: "Calculations in Plasma Physics Accuracy vs Speed"
date: 2021-10-20
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/jedrzej_walkowiak.png
speaker: "Dr. Jędrzej Walkowiak"
affiliation: "Institute of Nuclear Physics Polish Academy of Sciences, Poland"
youtube_id: "K-zdTJk240M"

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
Plasma physics is probably one of the most complicated fields to deal with. It involves so many phenomena, that it is extremely difficult, from the computation point of view, to obtain reliable results in a reasonable time. Therefore, without dedicated computation tools it would not be possible to carry on with the fusion project. As unintuitive it might be, sometimes the way to the result which more accurately reflects reality is not by developing more accurate models, but by finding their approximations. The key issue is computation time, which is usually the main constraint on the usability of the model in practical application. There are cases, when reducing the complexity of the models, which allows us to include more phenomena into our computation code. This eventually gives better results than just improving the basic physical model. There is also another level of fast computations, when we try to obtain the results in real time. This grants us certain benefits in magnetic confinement of plasma, but most of the algorithms cannot achieve the required speed. New approaches, like neural networks, can help in solving complicated problems in time scales unattainable before.
