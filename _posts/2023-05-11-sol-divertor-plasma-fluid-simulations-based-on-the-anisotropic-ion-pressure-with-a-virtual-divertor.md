---
title: "SOL-divertor plasma fluid simulations based on the anisotropic ion pressure with a virtual divertor"
date: 2023-05-11
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/satoshi_togo.jpg
speaker: "Satoshi Togo"
affiliation: "Plasma Research Center, University of Tsukuba, Japan"
youtube_id: "1ZN6EsHpIi0"
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
Improving scrape-off layer (SOL)-divertor plasma fluid models is highly required to design DEMO divertors. As an alternative to the conventional Braginskii’s plasma fluid model, we have been developing one based on the anisotropic ion pressure which we call AIP model. The parallel viscous flux term, which is an approximation of the anisotropic component of the ion pressure, is excluded in AIP model by directly describing the fluid equations in terms of the parallel and perpendicular ion pressures. That also makes it possible to exclude an explicit use of the Bohm criterion as the sheath boundary condition. Instead, a virtual divertor (VD) model has been incorporated within AIP model which reproduces effects of a sheath region by setting artificial volumetric sink terms in a virtual region beyond a sheath edge. It is demonstrated that the Bohm criterion can be automatically satisfied including some supersonic flow cases. A direct comparison between the Braginskii’s and AIP model shows that there can be a qualitative deviation of solutions between them in a rare collisional plasmas.
