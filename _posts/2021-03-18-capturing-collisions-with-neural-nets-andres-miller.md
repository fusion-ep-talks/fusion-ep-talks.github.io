---
title: "Capturing collisions with neural nets | Andres Miller"
date: 2021-03-18
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/default_teaser.png
speaker: "TBD"
affiliation: "TBD"
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
🖥️ Presenter for the FusionEPtalks #46 is Andres Miller, 1st year graduate student at MIT's Nuclear science and Engineering department, USA.

🎧 Hosted by Alexis, FusionEPtalks team 🎤

💬 Contact us directly on talk@fusion-ep.eu or use the comments to ask questions!

Visit the website https://fusionep-talks.egyplasma.com​​ for getting updates about the upcoming events.

Date: February 22nd, 2021

Conspectus: 
Machine learning, specifically convolutional neural networks, is used to examine the possibility of accelerating the solution to a partial integro-differential equation, the Fokker-Planck-Landau collision operator. This is part of the governing equation in the particle-in-cell code, XGC, which is used to study turbulence in fusion energy devices. In particular, training has involved borrowing network architectures used for the computer vision task of semantic segmentation. The neural network emphasizes physics-inspired learning, where it is taught to respect physical conservation constraints of the collision operator by including them in the training loss. It uses a penalization method that enforces the constraints of the system and integrates error in the conservation properties into the loss function. During training, quantities representing the density, momentum, and energy for all species of the system are calculated, mirroring the procedure in XGC. This simple training has produced a median relative loss the order of 10-4, which shows promise. The run time for the current iterative solver of the operator in XGC is O(n2), where n is the number of plasma species. As the code begins to attack problems including a larger number of species, the collision operator will become expensive computationally, making the neural network solver even more important, especially since the neural network training only scales as O(n). A wide enough range of collisionality has been considered in the training data to ensure the full domain of collision physics is captured. Further work includes expansion of the network to include multiple plasma species and the use of more sophisticated optimization techniques.

Chapters
00:00:05 - Speaker bio
00:01:19 - Speaker intro
00:02:11 - Outline
00:03:13 - Background 
00:08:00 - Neural networks (overview)
00:10:06 - Computer Vision - Image Recognition
00:12:43 - Computer Vision - Semantic Segmentation
00:15:04 - Technique for Collision Operator
00:23:12 - Fixed Penalty Method
00:25:44 - Architecture and Training
00:34:37 - Conclusion
00:38:42 - Q&A session
 
🌍 Fusion-EP Talks is a student-led seminar of the European Master In Fusion Science and Engineering program - 📚 join our international degree @ http://www.em-master-fusion.org​​​ 

📱FOLLOW US ON SOCIAL MEDIA📱
___________________________________

➤ Facebook : https://www.facebook.com/fusioneptalks​​​
➤ LinkedIn : https://www.linkedin.com/company/fusion-ep-talks
