---
title: "Capturing collisions with neural nets"
date: 2021-02-22
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/andres_miller.png
speaker: "Andres Miller"
affiliation: "MIT, US"
youtube_id: "yvqBZRAoE5o"
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
Machine learning, specifically convolutional neural networks, is used to examine the possibility of accelerating the solution to a partial integro-differential equation, the Fokker-Planck-Landau collision operator. This is part of the governing equation in the particle-in-cell code, XGC, which is used to study turbulence in fusion energy devices. In particular, training has involved borrowing network architectures used for the computer vision task of semantic segmentation. The neural network emphasizes physics-inspired learning, where it is taught to respect physical conservation constraints of the collision operator by including them in the training loss. It uses a penalization method that enforces the constraints of the system and integrates error in the conservation properties into the loss function. During training, quantities representing the density, momentum, and energy for all species of the system are calculated, mirroring the procedure in XGC. This simple training has produced a median relative loss the order of 10-4, which shows promise. The run time for the current iterative solver of the operator in XGC is O(n2), where n is the number of plasma species. As the code begins to attack problems including a larger number of species, the collision operator will become expensive computationally, making the neural network solver even more important, especially since the neural network training only scales as O(n). A wide enough range of collisionality has been considered in the training data to ensure the full domain of collision physics is captured. Further work includes expansion of the network to include multiple plasma species and the use of more sophisticated optimization techniques.
