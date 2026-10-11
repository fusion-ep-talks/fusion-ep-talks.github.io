---
title: "My experience with ill-posed problems (tomography, deconvolution)"
date: 2023-04-27
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/jan_m.jpg
speaker: "Dr. Jan Mlynář"
affiliation: "Czech Technical University, Czech Republic"
youtube_id: "TrKnby0ke-I"
author_profile: false
---

**Speaker:** {{ page.speaker }}  
**Position & Institution:** {{ page.affiliation }}  
**Date:** {{ page.date | date: "%B %d, %Y" }}  

<div style="clear: both; margin-top: 1.5rem;"></div>

### Recording

{% include video id=page.youtube_id provider="youtube" %}

<p style="text-align: center; margin-top: 1.25rem; display: flex; justify-content: center; gap: 0.75rem; flex-wrap: wrap;">
  <a href="https://www.youtube.com/watch?v={{ page.youtube_id }}" target="_blank" rel="noopener noreferrer" class="btn btn--primary">
    <i class="fab fa-youtube"></i> Watch on YouTube
  </a>
</p>

---

### Abstract
In tokamak data analyzes we are often dealing with ill-posed problems where sparse or erroneous data may seriously hamper the analysis result and produce artifacts. In my talk I shall briefly define ill-posedness, explain the cases of plasma tomography and spectral deconvolution and outline some basic ideas on how to treat the ill-posed problems using constraints. I will also explain the procedure that allowed me to consider the results of my analyses dependable and reliable contributions to tokamak data analyses.
