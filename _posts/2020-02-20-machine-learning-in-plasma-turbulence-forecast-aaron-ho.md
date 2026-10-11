---
title: "Machine learning in plasma turbulence forecast"
date: 2020-02-20
categories:
  - talks
tags:
  - fusion
  - plasma-physics
header:
  teaser: /assets/images/talks_teaser/aaron_ho.png
speaker: "Aaron Ho"
affiliation: "DIFFER, Nederlands"
youtube_id: "r6IY95Xwfmw"
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
In order to support the development and operation of large-scale high performance fusion devices, such as ITER, the predictive capabilities of plasma integrated modelling must be tested and further developed. These predictive models can then be used for applications such as experimental scenario optimization and control-oriented modelling, although the current state of the art models are limited by their computational time. One such example is plasma microturbulence, the dominant transport mechanism within present high-performance tokamaks, has been successfully modeled using gyrokinetic (GK) theory. However, the computational times of full nonlinear GK codes prohibit their use in the aforementioned applications. Reduced formulations of these equations have resulted in quasilinear turbulent
transport models, such as QuaLiKiz and TGLF, which are orders of magnitude faster but still not fast enough for the desired application. Recent work has applied neural network (NN) regressions to create surrogate models trained using these reduced models, showing promising results in terms of bridging this gap while retaining the required accuracy in integrated modelling applications.
The current QuaLiKiz NN surrogate model accepts 14 dimensionless local plasma parameters, which sufficiently cover the input space of the underlying physics model. Multivariate sampling was used to avoid the prohibitively large number of points required for a 14D hypercube grid scan. Since there are no explicit distribution functions for the input plasma parameters to be used
for sampling, the inputs were instead sampled directly from JET experimental profiles and experimental uncertainties obtained via Gaussian process regression (GPR) techniques. Due to the unordered nature of the sampled inputs and the inherent variation
in the quality of experimental profiles and their fits, data clustering algorithms were combined to effectively filter the 14D data set. In addition, multiple independent networks trained on identical data were combined into committee NNs. Evaluation of the statistics of these committees provided information regarding the density of points inside the training set, allowing for a quick and implicit
determination of its applicability inside a given input parameter space. Future work will involve using these new fast surrogates within offline optimization exercises. 19:00 (CET): Helicon Plasmas in Fusion from Foisal B.T. Siddiki. For more information visit the event page in Facebook https://www.facebook.com/events/1506006309571327/ .


📕 Facebook - https://www.facebook.com/fusioneptalks/
