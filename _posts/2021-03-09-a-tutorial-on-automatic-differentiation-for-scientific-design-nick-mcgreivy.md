---
title: "A tutorial on automatic differentiation for scientific design"
date: 2021-03-09
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/nick_mcgreivy.png
speaker: "Nick McGreivy"
affiliation: "Princeton University, US"
youtube_id: "wNiulgucIbc"
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
Automatic differentiation (AD) is a numerical technique for computing the derivative of a function specified as a computer program. Although AD was invented decades ago, it wasn’t until the recent interest in machine learning and the associated development of high-quality automatic differentiation frameworks that the benefits of AD in physics were more widely recognized. In this tutorial, I introduce AD. By the end of the tutorial, you will hopefully understand the fundamentals of how AD works in theory and how it is used in practice. For a short, 5-minute introduction to AD, feel free to read this https://twitter.com/NMcgreivy/status/1351706692317138945?s=20 and this https://twitter.com/NMcgreivy/status/1286057985987563525?s=20.
