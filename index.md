---
layout: single
classes: wide
title: "Fusion EP Talks"
excerpt: "Bridging plasma physics research, academic networking, and open science across the global fusion community."
header:
  overlay_color: "#1a1e24"
  overlay_filter: "0.45"
  overlay_image: /assets/images/fondo.webp
  og_image: /assets/images/site-preview.png
  actions:
    - label: "Explore Seminars"
      url: "/talks/"
    - label: "About the Initiative"
      url: "/about/"
author_profile: false
---

<style>
  /* Featured Next Talk Card */
  .featured-talk-card {
    background: #f8fafc;
    border: 1px solid #e2e8f0;
    border-left: 6px solid #009639;
    border-radius: 8px;
    padding: 1.75rem 2rem;
    margin: 1.5rem 0 3rem 0;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.04);
  }
  .featured-badge {
    display: inline-block;
    background-color: #f2b200;
    color: #ffffff;
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    padding: 0.2rem 0.6rem;
    border-radius: 4px;
    margin-bottom: 0.8rem;
  }

  /* Metric Counters Strip */
  .metrics-strip {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
    text-align: center;
    margin: 3rem 0;
    padding: 1.5rem 0;
    border-top: 1px solid #e5e7eb;
    border-bottom: 1px solid #e5e7eb;
  }
  .metric-item strong {
    display: block;
    font-size: 2.2rem;
    color: #009639;
    line-height: 1.1;
  }
  .metric-item span {
    font-size: 0.88rem;
    color: #64748b;
    font-weight: 500;
  }

  /* Feature Columns Grid */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.5rem;
    margin: 2.5rem 0 3.5rem 0;
  }
  .feature-box {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    padding: 1.5rem;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.03);
  }
  .feature-box h4 {
    margin-top: 0.5rem;
    margin-bottom: 0.6rem;
    color: #1e293b;
    font-size: 1.1rem;
  }
  .feature-box p {
    font-size: 0.9rem;
    line-height: 1.5;
    color: #475569;
    margin: 0;
  }

  /* Call To Action Box */
  .cta-banner {
    background: linear-gradient(135deg, #009639 0%, #006827 100%);
    color: #ffffff;
    padding: 2.25rem;
    border-radius: 10px;
    text-align: center;
    margin: 3.5rem 0 1.5rem 0;
  }
  .cta-banner h3 {
    color: #ffffff;
    margin-top: 0;
    margin-bottom: 0.6rem;
  }
  .cta-banner p {
    color: #e2e8f0;
    font-size: 0.95rem;
    max-width: 650px;
    margin: 0 auto 1.5rem auto;
  }
</style>

<!-- ======================================================================= -->
<!-- 1. DYNAMIC NEXT UPCOMING TALK FINDER                                    -->
<!-- ======================================================================= -->
{% assign all_sorted_posts = site.posts | sort: "date" %}
{% assign next_talk = nil %}

{% for item in all_sorted_posts %}
  {% if item.youtube_id == nil or item.youtube_id == "" %}
    {% assign next_talk = item %}
    {% break %}
  {% endif %}
{% endfor %}

{% if next_talk %}
<div class="featured-talk-card">
  <span class="featured-badge">Next Upcoming Seminar</span>
  <h2 style="margin-top: 0; margin-bottom: 0.6rem; font-size: 1.5rem; color: #1e293b;">
    <a href="{{ next_talk.url | relative_url }}" style="text-decoration: none; color: inherit;">
      {{ next_talk.title }}
    </a>
  </h2>
  
  <p style="margin-bottom: 1rem; color: #475569; font-size: 0.95rem;">
    📅 <strong>{{ next_talk.date | date: "%B %d, %Y" }}</strong>
    {% if next_talk.time %} — {{ next_talk.time }}{% endif %}
    {% if next_talk.speaker %}
      &nbsp;|&nbsp; 👤 <strong>{{ next_talk.speaker }}</strong>
    {% endif %}
    {% if next_talk.affiliation %}
      <span style="color: #64748b;">({{ next_talk.affiliation }})</span>
    {% endif %}
    &nbsp;|&nbsp; 📍 <em>Online via Zoom</em>
  </p>

  {% if next_talk.excerpt %}
  <div style="margin-bottom: 1.25rem; color: #334155; line-height: 1.6; font-size: 0.92rem;">
    {{ next_talk.excerpt | markdownify }}
  </div>
  {% endif %}

  <div style="display: flex; gap: 0.75rem; flex-wrap: wrap;">
    {% if next_talk.registration_url %}
      <a href="{{ next_talk.registration_url }}" target="_blank" rel="noopener noreferrer" class="btn btn--primary" style="margin: 0;">
        Register for this Talk (Free)
      </a>
    {% else %}
      <a href="{{ next_talk.url | relative_url }}" class="btn btn--primary" style="margin: 0;">
        Register & Details
      </a>
    {% endif %}
    <a href="{{ '/talks/' | relative_url }}" class="btn btn--inverse" style="margin: 0;">
      Browse All Talks
    </a>
  </div>
</div>
{% else %}
<!-- Fallback card displayed when all recorded talks have concluded -->
<div class="featured-talk-card" style="border-left-color: #64748b;">
  <span class="featured-badge" style="background-color: #64748b;">Announcements</span>
  <h2 style="margin-top: 0; margin-bottom: 0.6rem; font-size: 1.4rem; color: #1e293b;">
    Upcoming Seminars in Preparation
  </h2>
  <p style="margin-bottom: 1.2rem; color: #475569; font-size: 0.95rem;">
    We are currently scheduling our next set of research talks. Check back soon for registration details, or explore our full library of recorded sessions.
  </p>
  <a href="{{ '/talks/' | relative_url }}" class="btn btn--primary" style="margin: 0;">
    Browse Recorded Talks
  </a>
</div>
{% endif %}

<!-- ======================================================================= -->
<!-- 2. IMPACT & COMMUNITY METRICS                                           -->
<!-- ======================================================================= -->
<div class="metrics-strip">
  <div class="metric-item">
    <strong>{{ site.posts.size }}+</strong>
    <span>Seminars & Discussions</span>
  </div>
  <div class="metric-item">
    <strong>20+</strong>
    <span>International Institutions</span>
  </div>
  <div class="metric-item">
    <strong>100%</strong>
    <span>Open Access & Non-Profit</span>
  </div>
</div>

<!-- ======================================================================= -->
<!-- 3. PROJECT PILLARS / HIGHLIGHTS                                         -->
<!-- ======================================================================= -->
### What We Do

<div class="features-grid">
  <div class="feature-box">
    <div style="font-size: 1.8rem;">🎓</div>
    <h4>Student-Led Seminars</h4>
    <p>Organized by master's and PhD researchers to discuss cutting-edge plasma theory, simulation benchmarks, and experimental diagnostics.</p>
  </div>
  <div class="feature-box">
    <div style="font-size: 1.8rem;">🎥</div>
    <h4>Open Archive</h4>
    <p>Full recordings, curated slide decks, and discussion logs available to the public on our YouTube channel and website archive.</p>
  </div>
  <div class="feature-box">
    <div style="font-size: 1.8rem;">🌐</div>
    <h4>Academic Networking</h4>
    <p>Connecting early-career researchers with leading labs, ITER consortia members, and private fusion initiatives worldwide.</p>
  </div>
</div>

---

<!-- ======================================================================= -->
<!-- 4. CALL FOR SPEAKERS (BANNER)                                           -->
<!-- ======================================================================= -->
<div class="cta-banner">
  <h3>Interested in Presenting Your Research?</h3>
  <p>
    Whether you are working on kinetic simulations, stellarator optimization, materials science, or diagnostic design, our platform welcomes PhD candidates and postdocs to share their progress.
  </p>
  <a href="{{ '/contact/' | relative_url }}" class="btn btn--light btn--large" style="margin: 0; color: #009639; font-weight: 700;">
    Submit a Talk Proposal
  </a>
</div>
