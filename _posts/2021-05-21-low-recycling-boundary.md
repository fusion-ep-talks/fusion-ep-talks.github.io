---
title: "The promise of a low recycling boundary"
date: 2021-05-21
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/anurag_maan.png
speaker: "Dr. Anurag Maan"
affiliation: "Princeton Plasma Physics Laboratory, US"
youtube_id: "NnOcebs233Q"

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
The Lithium Tokamak eXperiment-beta (LTX-beta) is attempting to answer key questions regarding the feasibility of operating a tokamak with a lithium boundary. Lithium coatings on high-Z plasma facing components (PFCs) in the LTX (LTX-beta predecessor) led to flat temperature profiles. The flat temperature profiles were observed along with a hot low density edge, implying a broad, collisionless Scrape-Off Layer (SOL). Additionally, in-vacuo analysis of PFCs indicated that evaporatively deposited lithium coatings appeared to be oxidized, while the ability to achieve good plasma performance was retained. Theory attributes flat temperature profiles to low recycling walls, which was assumed to be due to hydrogen binding with elemental lithium to form lithium hydride. The presence of oxidized lithium, however, raises questions regarding the exact mechanism of hydrogen retention in LTX. These questions were investigated using a new Sample Exposure Probe (SEP) for detailed in-vacuo analysis of PFC samples was designed and commissioned for LTX-beta. The SEP is equipped with a vacuum suitcase capable of transporting samples representative of LTX-beta outer mid-plane PFCs under high vacuum to a stand-alone high resolution XPS system. Surface analysis using the SEP was performed with sufficient energy resolution to identify for the first time, the compounds that grow on evaporative lithium coatings inside a tokamak. This was the first demonstration that a vacuum suitcase can afford a solution that is simpler in design and affords more flexibility than building material characterization test stands for installation on a tokamak. The results indicate that Lithium Oxide and Lithium Hydroxide are prime surface constituents of Lithium PFCs. Their presence substantiates the hypothesis that lithium oxide grows on elemental lithium before the growth transitions to lithium hydroxide for LTX-beta like vacuum conditions. It is further indicated that Lithium Oxide improves plasma performance in comparison to Lithium Hydroxide by both sequestering oxygen and increasing hydrogen retention. The talk will also outline current efforts that aim at estimating recycling in LTX-beta.
