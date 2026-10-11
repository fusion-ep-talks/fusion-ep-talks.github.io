---
title: "2-D robotic control of a plasma probe"
date: 2019-11-14
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/johannes_lips_2.png
speaker: "Johannes Lips"
affiliation: "Université de Lorraine, France"
youtube_id: "v08uqRiNNz4"
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
This talk will discuss the upgrade of the control system of a 2-D probe at TJ-K (University of Stuttgart), which the speaker was responsible for as a first-year master student. Mounted on a manipulator, the probe can perform single and swept measurements. The control system can locate the tip of the probe at any position within a 2-D section of the stellarator. Focus will be on practical issues such as hardware-software compatibility, error propagation in diagnostic devices and different bus-systems in desktop computers. An introduction to LabView is provided as the audience is walked through the upgrading process.
