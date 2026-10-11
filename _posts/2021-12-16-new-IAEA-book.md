---
title: "New IAEA book: “Fundamentals of Magnetic Fusion Technology”"
date: 2021-12-16
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/guido_van_oost.png
speaker: "Dr. Guido Van Oost"
affiliation: "Ghent University, Belgium"
youtube_id: "kek1pqdfT8M"

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
The main objective of this textbook is to contribute to the consolidation and better exploitation of the achievements already reached and to tackle the present challenges in preparing the workforce in the different areas, with special attention to continuous professional development and life-long learning. This textbook is edited on the occasion of the 60th anniversary of Fusion Research. The book covers a wide range of topics, and will also be useful for specialists from academia, research institutions and companies who want to acquire knowledge of other areas in magnetic fusion technology, as well as for a wider range of readers interested in the establishment of magnetic fusion as an energy source.
