---
title: "Retention and recycling of D/T fuels in a fusion reactor"
date: 2022-01-18
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/tetsuo_tanabe.png
speaker: "Prof. Dr. Tetsuo Tanabe"
affiliation: "Osaka City University, Japan"
youtube_id: "HEzjOOqvGmw"

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
In ITER and a fusion reactor, tritium (T) and deuterium (D) are used as fuels. Because of resource scarcity and radioactivity of T, special care is required and we will face various restrictions in using huge amounts of tritium (T) for DT burning. Required are simultaneous achievements of self-sufficiency of T fuel with T breeding, efficient D-T burning, and T safety. Detailed requirements to keep T economy are, 1. Power generation compatible with T breeding 2. Having enough margin in T breeding 3. Huge T through-put due to poor burning efficiency 4. Optimized control of DT fueling for efficient DT burning 5. Quantitative analysis of D and T in plasma and in materials 6. Unknown isotope effects between D and T in burning plasma and T recycling systems 7. Large in-vessel T inventory hard to remove They are related to today’s talk (Retention and recycling of D/T fuels) And requirements to keep T safety are (1) Unavoidable permeation and leakage in T handling systems, (2) Isotope separation and fuel refinement (Contamination by H is concerned), (3) Easy transfer of contamination through HTO, DTO, and OBT (Organic Binding T) (4) Significantly large decontamination factor required (more than 10^-6 ) in T handling systems, and (5) T safety required under severe accidents. These are not discussed here but quite important to establish a fusion reactor as an energy source. Please refer a published book for ex. “Tritium as a fuel of fusion reactor, Springer 2017, DOI 10.1007/978-4-431-56460-7”. The requirements to keep T economy are directly correlated to fuel recycling at plasma facing surfaces, because T inventory in the plasma facing materials is the largest except fuel reservoirs. In addition, the fuel recycling is a critical issue for efficient D-T burning. Nevertheless, the fuel retention and recycling in a fusion reactor is not well estimated. In this talk described are after general introduction on tritium in nature and as a fuel of D-T fusion reactor and what are required for T use in a fusion reactor, “Fundamentals of interactions of hydrogen with plasma facing materials” and “Hydrogen retention in present tokamaks” in which fuel retention rates at steady state operation or inventory in PFM and their difference between low Z (Carbon) wall and high Z (Tungsten) wall are explained. Finally given are summary and perspective on research works of the retention and recycling of D/T fuels.
