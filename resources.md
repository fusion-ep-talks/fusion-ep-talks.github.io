---
title: "Resources: Learning Library, Code & Simulation Gallery"
layout: single
permalink: /resources/
classes: wide
author_profile: false
---
 
<style>
  /* ---------- Section switcher / tabs ---------- */
  .resource-nav {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin: 1.5rem 0 2.5rem 0;
    border-bottom: 2px solid #e5e7eb;
    padding-bottom: 0.5rem;
  }
  .resource-nav-link {
    font-weight: 700;
    font-size: 1.05rem;
    color: #4b5563;
    text-decoration: none !important;
    padding: 0.5rem 0.8rem;
    border-radius: 6px;
    transition: all 0.2s;
  }
  .resource-nav-link:hover {
    color: #009639;
    background: #f3f4f6;
  }
  .resource-section {
    margin-bottom: 3.5rem;
    scroll-margin-top: 1rem;
  }
  .resource-section > h2 { margin-top: 0; }
  .resource-lead {
    color: #6b7280;
    font-size: 0.95rem;
    margin-bottom: 1.5rem;
  }
  /* ---------- Generic grid ---------- */
  .resource-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
  }
  /* ---------- Learning Library ---------- */
  .lib-controls {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    align-items: center;
    margin-bottom: 1rem;
  }
  .lib-search { flex: 1 1 280px; }
  .lib-search input[type="search"] {
    width: 100%;
    padding: 0.6rem 0.9rem;
    border: 1px solid #d1d5db;
    border-radius: 8px;
    font-size: 0.95rem;
    background: #ffffff;
    color: #111827;
  }
  .lib-search input[type="search"]:focus {
    outline: none;
    border-color: #009639;
    box-shadow: 0 0 0 3px rgba(0, 150, 57, 0.15);
  }
  .lib-controls select {
    padding: 0.55rem 0.8rem;
    border: 1px solid #d1d5db;
    border-radius: 8px;
    font-size: 0.88rem;
    background: #ffffff;
    color: #374151;
    margin: 0;
  }
  .lib-controls select:focus {
    outline: none;
    border-color: #009639;
  }
  .lib-clear {
    appearance: none;
    border: none;
    background: none;
    color: #009639;
    font-size: 0.85rem;
    font-weight: 600;
    cursor: pointer;
    text-decoration: underline;
    padding: 0.3rem 0.4rem;
  }
  .res-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin: 0 0 1.25rem 0;
  }
  .res-chip {
    appearance: none;
    border: 1px solid #d1d5db;
    background-color: #ffffff;
    color: #374151;
    font-size: 0.82rem;
    font-weight: 600;
    padding: 0.35rem 0.85rem;
    border-radius: 9999px;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
  }
  .res-chip:hover {
    border-color: #009639;
    color: #009639;
  }
  .res-chip.active {
    background-color: #009639;
    border-color: #009639;
    color: #ffffff;
    box-shadow: 0 2px 4px rgba(0, 150, 57, 0.2);
  }
  .res-count { font-weight: 500; opacity: 0.75; margin-left: 0.15rem; }
  .lib-status {
    font-size: 0.85rem;
    color: #6b7280;
    margin: 0 0 1rem 0;
  }
  .lib-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.25rem;
    margin-bottom: 2rem;
  }
  .lib-card {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    padding: 1.1rem 1.25rem;
    box-shadow: 0 2px 6px rgba(0,0,0,0.04);
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .lib-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 14px rgba(0,0,0,0.08);
  }
  .lib-card.is-hidden { display: none !important; }
  .lib-card h3 {
    margin: 0;
    font-size: 1.05rem;
    line-height: 1.3;
    color: #111827;
  }
  .lib-card h3 a {
    color: inherit;
    text-decoration: none;
  }
  .lib-card h3 a:hover {
    color: #009639;
    text-decoration: underline;
  }
  .lib-meta { font-size: 0.82rem; color: #6b7280; margin: 0; }
  .lib-desc { font-size: 0.88rem; color: #4b5563; line-height: 1.5; margin: 0; }
  .lib-badges { display: flex; flex-wrap: wrap; gap: 0.35rem; }
  .lib-badge {
    display: inline-block;
    font-size: 0.7rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.4px;
    padding: 0.15rem 0.5rem;
    border-radius: 4px;
  }
  .lib-badge--type     { background: #dbeafe; color: #1e40af; }
  .lib-badge--level    { background: #f3f4f6; color: #4b5563; }
  .lib-badge--lang     { background: #e0f2fe; color: #0369a1; }
  .lib-badge--featured { background: #fef3c7; color: #b45309; }
  .lib-badge--access   { background: #fee2e2; color: #b91c1c; }
  .lib-badge--free     { background: #d1fae5; color: #047857; }
  .lib-topics { display: flex; flex-wrap: wrap; gap: 0.3rem; margin-top: auto; padding-top: 0.25rem; }
  .topic-pill {
    font-size: 0.72rem;
    background: #f3f4f6;
    color: #4b5563;
    padding: 0.15rem 0.55rem;
    border-radius: 9999px;
  }
 
  .res-empty {
    padding: 1.5rem;
    margin-bottom: 2rem;
    text-align: center;
    color: #6b7280;
    background: #f9fafb;
    border: 1px dashed #d1d5db;
    border-radius: 8px;
  }
  .res-empty[hidden], .lib-clear[hidden] { display: none; }
  /* ---------- Code Workshop Cards ---------- */
  .workshop-card {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    padding: 1.5rem;
    box-shadow: 0 2px 6px rgba(0,0,0,0.04);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .workshop-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 14px rgba(0,0,0,0.08);
  }
  .badge-lang {
    display: inline-block;
    font-size: 0.75rem;
    font-weight: 700;
    padding: 0.2rem 0.55rem;
    border-radius: 4px;
    background: #e0f2fe;
    color: #0369a1;
    text-transform: uppercase;
  }
  .badge-level {
    display: inline-block;
    font-size: 0.75rem;
    font-weight: 600;
    padding: 0.2rem 0.55rem;
    border-radius: 4px;
    background: #f3f4f6;
    color: #4b5563;
    margin-left: 0.4rem;
  }
  /* ---------- Visual Asset Card ---------- */
  .visual-card {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 6px rgba(0,0,0,0.04);
    display: flex;
    flex-direction: column;
  }
  .visual-media {
    width: 100%;
    background: #111827;
    display: flex;
    align-items: center;
    justify-content: center;
    aspect-ratio: 16 / 9;
    overflow: hidden;
  }
  /* "contain" so plots, axes and video controls are never cropped */
  .visual-media img,
  .visual-media video {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  .visual-body {
    padding: 1.25rem;
    display: flex;
    flex-direction: column;
    flex: 1;
    justify-content: space-between;
  }
  .visual-credit {
    font-size: 0.78rem;
    color: #6b7280;
    margin: 0 0 0.5rem 0;
  }
  .code-drawer {
    background: #f9fafb;
    border-top: 1px solid #e5e7eb;
    padding: 0.75rem 1.25rem;
    font-size: 0.85rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  /* ---------- Fallback box (shown only if everything is empty) ---------- */
  .under-construction-box {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    padding: 2.5rem 2rem;
    text-align: center;
    max-width: 780px;
    margin: 2rem auto;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  }
  /* ---------- Screen-reader-only text ---------- */
  .sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border: 0;
  }
</style>
 
{% comment %}
==============================================================================
 BUILD STEP (prepares variables, outputs nothing)
 
 Data files (all in _data/):
   resources_library.yml    -> topics / types / levels lists + "entries"
   resources_notebooks.yml  -> list of notebooks
   resources_visuals.yml    -> list of simulations / animations
 
 A section is rendered only if its file has at least one entry.
 If all three are empty, a "coming soon" box is shown instead.
 
 URL rule used everywhere below: values containing "://" are used as they
 are (external); anything else is treated as a path inside this site and
 goes through relative_url (so it works with or without a baseurl).
==============================================================================
{% endcomment %}
{%- assign lib = site.data.resources_library -%}
{%- assign lib_entries = lib.entries -%}
{%- assign lib_count = lib_entries | size -%}
{%- assign nb_entries = site.data.resources_notebooks -%}
{%- assign nb_count = nb_entries | size -%}
{%- assign vis_entries = site.data.resources_visuals -%}
{%- assign vis_count = vis_entries | size -%}
{%- assign total_count = lib_count | plus: nb_count | plus: vis_count -%}
 
{% if total_count == 0 %}
 
<div class="under-construction-box">
  <div style="font-size: 2.5rem; margin-bottom: 1rem;">⚙️</div>
  <h2 style="margin-top: 0; margin-bottom: 0.75rem; color: #111827;">Section Under Development</h2>
  <p style="font-size: 1.05rem; color: #4b5563; line-height: 1.6; margin-bottom: 1.5rem;">
    We are curating a library of learning resources, interactive computational notebooks and reproducible simulation animations linked to our seminar series.
  </p>
  <span style="display: inline-block; background: #e0f2fe; color: #0369a1; font-weight: 600; font-size: 0.85rem; padding: 0.35rem 0.85rem; border-radius: 9999px;">
    🚀 Launching Soon
  </span>
</div>
{% else %}
 
<nav class="resource-nav" aria-label="Sections of this page">
  {% if lib_count > 0 %}<a href="#library" class="resource-nav-link">📚 Learning Library</a>{% endif %}
  {% if nb_count > 0 %}<a href="#notebooks" class="resource-nav-link">💻 Code Notebooks</a>{% endif %}
  {% if vis_count > 0 %}<a href="#gallery" class="resource-nav-link">🎬 Simulation Gallery</a>{% endif %}
</nav>
<p>
  Welcome to the resources hub of <strong>Fusion EP Talks</strong>: a curated place to learn and study plasma physics and nuclear fusion, together with our own open computational material.
</p>
{% endif %}
 
 
{% comment %}
==============================================================================
 SECTION 1: LEARNING LIBRARY
==============================================================================
{% endcomment %}
{% if lib_count > 0 %}
 
{%- assign lib_types = lib.types -%}
{%- assign lib_levels = lib.levels -%}
 
{%- comment -%} Distinct languages (blank language = English) {%- endcomment -%}
{%- assign lang_str = "" -%}
{%- for e in lib_entries -%}
  {%- assign l = e.language | default: "English" | strip -%}
  {%- assign lang_str = lang_str | append: l | append: "|" -%}
{%- endfor -%}
{%- assign lang_list = lang_str | split: "|" | uniq | sort -%}
 
{%- comment -%} Order: featured first, then A-Z (case-insensitive) {%- endcomment -%}
{%- assign sorted_entries = lib_entries | sort_natural: "title" -%}
{%- assign featured_entries = sorted_entries | where: "featured", true -%}
{%- assign other_entries = sorted_entries | where_exp: "x", "x.featured != true" -%}
{%- assign ordered_entries = featured_entries | concat: other_entries -%}
 
<section id="library" class="resource-section">
  <h2>📚 Learning Library</h2>
  <p class="resource-lead">
    A curated collection of external websites, videos, lecture notes, courses, books and software to learn and study plasma physics and nuclear fusion. These resources belong to their respective authors; we only link to them.
  </p>
  <div class="lib-controls">
    <div class="lib-search">
      <label for="lib-search-input" class="sr-only">Search the library</label>
      <input type="search" id="lib-search-input" placeholder="Search by title, author or keyword…" autocomplete="off">
    </div>
    {% if lib_types %}
    <label for="lib-filter-type" class="sr-only">Filter by type</label>
    <select id="lib-filter-type">
      <option value="">All types</option>
      {% for t in lib_types %}<option value="{{ t[0] | escape }}">{{ t[1] }}</option>{% endfor %}
    </select>
    {% endif %}
 
    {% if lib_levels %}
    <label for="lib-filter-level" class="sr-only">Filter by level</label>
    <select id="lib-filter-level">
      <option value="">All levels</option>
      {% for lv in lib_levels %}<option value="{{ lv[0] | escape }}">{{ lv[1] }}</option>{% endfor %}
    </select>
    {% endif %}
 
    {% if lang_list.size > 1 %}
    <label for="lib-filter-lang" class="sr-only">Filter by language</label>
    <select id="lib-filter-lang">
      <option value="">All languages</option>
      {% for l in lang_list %}<option value="{{ l | escape }}">{{ l }}</option>{% endfor %}
    </select>
    {% endif %}
 
    <button type="button" class="lib-clear" id="lib-clear" hidden>Clear filters</button>
  </div>
  <div class="res-chips" role="group" aria-label="Filter by topic">
    <button type="button" class="res-chip active" data-topic="all" aria-pressed="true">All topics <span class="res-count"></span></button>
    {% for topic in lib.topics %}
    <button type="button" class="res-chip" data-topic="{{ topic | escape }}" aria-pressed="false">{{ topic }} <span class="res-count"></span></button>
    {% endfor %}
  </div>
  <p class="lib-status" id="lib-status" role="status" aria-live="polite"></p>
  <p class="res-empty" id="lib-empty" hidden>No resources match these filters. Try a different search, or suggest one using the button at the bottom of the page.</p>
  <div class="lib-grid">
  {%- for e in ordered_entries -%}
    {%- assign e_type = e.type | append: "" | downcase | strip -%}
    {%- assign e_level = e.level | append: "" | downcase | strip -%}
    {%- assign e_lang = e.language | default: "English" | strip -%}
    {%- assign e_topics = e.topics | join: "|" -%}
    {%- assign e_type_label = lib_types[e_type] | default: "Resource" -%}
    {%- assign e_level_label = lib_levels[e_level] -%}
    {%- assign e_access = e.access | append: "" | downcase | strip -%}
    {%- assign e_link = e.link | append: "" | strip -%}
    {%- if e_link != "" -%}{%- unless e_link contains "://" -%}{%- assign e_link = e_link | relative_url -%}{%- endunless -%}{%- endif -%}
 
    {%- capture e_search -%}{{ e.title }} {{ e.author }} {{ e.description }} {{ e_topics | replace: "|", " " }} {{ e_type_label }} {{ e_lang }}{%- endcapture -%}
    {%- assign pill_list = e_topics | split: "|" %}
    <article class="lib-card" data-type="{{ e_type | escape }}" data-level="{{ e_level | escape }}" data-lang="{{ e_lang | escape }}" data-topics="{{ e_topics | escape }}" data-search="{{ e_search | downcase | strip_newlines | escape }}"{% if e.last_checked %} data-last-checked="{{ e.last_checked }}"{% endif %}>
      <div class="lib-badges">
        {% if e.featured == true %}<span class="lib-badge lib-badge--featured">⭐ Start here</span>{% endif %}
        <span class="lib-badge lib-badge--type">{{ e_type_label }}</span>
        {% if e_level_label %}<span class="lib-badge lib-badge--level">{{ e_level_label }}</span>{% endif %}
        <span class="lib-badge lib-badge--lang">{{ e_lang }}</span>
        {% case e_access %}
          {% when "free" %}<span class="lib-badge lib-badge--free">Free</span>
          {% when "paywalled" %}<span class="lib-badge lib-badge--access">🔒 Paywalled</span>
          {% when "registration" %}<span class="lib-badge lib-badge--access">📝 Free account required</span>
        {% endcase %}
      </div>
 
      <h3>{% if e_link != "" %}<a href="{{ e_link }}" target="_blank" rel="noopener noreferrer">{{ e.title }} &rarr;</a>{% else %}{{ e.title }}{% endif %}</h3>
 
      {% if e.author and e.author != "" %}<p class="lib-meta">{{ e.author }}</p>{% endif %}
      {% if e.description and e.description != "" %}<p class="lib-desc">{{ e.description }}</p>{% endif %}
 
      {% if pill_list.size > 0 %}<div class="lib-topics">{% for t in pill_list %}<span class="topic-pill">{{ t }}</span>{% endfor %}</div>{% endif %}
    </article>
  {%- endfor %}
  </div>
</section>
{% endif %}
 
 
{% comment %}
==============================================================================
 SECTION 2: CODE NOTEBOOKS
==============================================================================
{% endcomment %}
{% if nb_count > 0 %}
 
<section id="notebooks" class="resource-section">
  <h2>💻 Interactive Code Notebooks & Tutorials</h2>
  <p class="resource-lead">
    Run directly in your browser with zero local installation using Google Colab, or clone the repository to run locally.
  </p>
  <div class="resource-grid">
  {%- for nb in nb_entries -%}
    {%- assign nb_level = nb.level | append: "" | downcase | strip -%}
    {%- assign nb_level_label = lib_levels[nb_level] | default: nb.level -%}
    {%- assign nb_colab = nb.colab_url | append: "" | strip -%}
    {%- if nb_colab != "" -%}{%- unless nb_colab contains "://" -%}{%- assign nb_colab = nb_colab | relative_url -%}{%- endunless -%}{%- endif -%}
    {%- assign nb_repo = nb.repo_url | append: "" | strip -%}
    {%- if nb_repo != "" -%}{%- unless nb_repo contains "://" -%}{%- assign nb_repo = nb_repo | relative_url -%}{%- endunless -%}{%- endif %}
    <div class="workshop-card">
      <div>
        <div style="margin-bottom: 0.75rem;">
          {% if nb.language %}<span class="badge-lang">{{ nb.language }}</span>{% endif %}
          {% if nb_level_label %}<span class="badge-level">{{ nb_level_label }}</span>{% endif %}
        </div>
        <h3 style="margin: 0 0 0.5rem 0; font-size: 1.25rem;">{{ nb.title }}</h3>
        {% if nb.description and nb.description != "" %}<p style="font-size: 0.9rem; color: #4b5563; line-height: 1.5;">{{ nb.description }}</p>{% endif %}
        {% if nb.author and nb.author != "" %}<p style="font-size: 0.8rem; color: #6b7280; margin: 0;">By {{ nb.author }}</p>{% endif %}
        <p style="font-size: 0.78rem; color: #6b7280; margin: 0.3rem 0 0 0;">License: {{ nb.license | default: "CC BY 4.0" }}</p>
      </div>
      {% if nb_colab != "" or nb_repo != "" %}
      <div style="margin-top: 1.2rem; display: flex; gap: 0.6rem; flex-wrap: wrap;">
        {% if nb_colab != "" %}<a href="{{ nb_colab }}" target="_blank" rel="noopener noreferrer" class="btn btn--primary" style="margin: 0; font-size: 0.8rem; padding: 0.4rem 0.8rem;"><i class="fas fa-play"></i> Run in Colab</a>{% endif %}
        {% if nb_repo != "" %}<a href="{{ nb_repo }}" target="_blank" rel="noopener noreferrer" class="btn btn--inverse" style="margin: 0; font-size: 0.8rem; padding: 0.4rem 0.8rem;"><i class="fab fa-github"></i> Repository</a>{% endif %}
      </div>
      {% endif %}
    </div>
  {%- endfor %}
  </div>
</section>
{% endif %}
 
 
{% comment %}
==============================================================================
 SECTION 3: SIMULATION & ANIMATION GALLERY
==============================================================================
{% endcomment %}
{% if vis_count > 0 %}
 
<section id="gallery" class="resource-section">
  <h2>🎬 Simulation & Animation Gallery</h2>
  <p class="resource-lead">
    Scientific assets generated for workshops and seminar companion materials. Unless a card states otherwise, you are free to reuse them in academic presentations or theses under <strong>CC BY 4.0</strong> attribution.
  </p>
  <div class="resource-grid">
  {%- for visual in vis_entries -%}
    {%- assign m = visual.media_url | append: "" | strip -%}
    {%- if m != "" -%}{%- unless m contains "://" -%}{%- assign m = m | relative_url -%}{%- endunless -%}{%- endif -%}
    {%- assign p = visual.poster_url | append: "" | strip -%}
    {%- if p != "" -%}{%- unless p contains "://" -%}{%- assign p = p | relative_url -%}{%- endunless -%}{%- endif -%}
    {%- assign c = visual.code_repo | append: "" | strip -%}
    {%- if c != "" -%}{%- unless c contains "://" -%}{%- assign c = c | relative_url -%}{%- endunless -%}{%- endif -%}
    {%- comment -%} File extension (query string ignored) decides video type and mime {%- endcomment -%}
    {%- assign m_ext = m | split: "?" | first | downcase | split: "." | last -%}
    {%- assign is_video = false -%}
    {%- assign mime = "" -%}
    {%- case m_ext -%}
      {%- when "mp4" -%}{%- assign is_video = true -%}{%- assign mime = "video/mp4" -%}
      {%- when "webm" -%}{%- assign is_video = true -%}{%- assign mime = "video/webm" -%}
      {%- when "ogv" -%}{%- assign is_video = true -%}{%- assign mime = "video/ogg" -%}
    {%- endcase -%}
    {%- if visual.media_type == "video" -%}{%- assign is_video = true -%}{%- endif -%}
    {%- if visual.media_type == "image" -%}{%- assign is_video = false -%}{%- endif -%}
 
    {%- assign v_license = visual.license | default: "CC BY 4.0" -%}
    {%- assign v_license_url = visual.license_url | append: "" | strip -%}
    {%- if v_license == "CC BY 4.0" and v_license_url == "" -%}{%- assign v_license_url = "https://creativecommons.org/licenses/by/4.0/" -%}{%- endif %}
    <div class="visual-card">
      {% if m != "" %}
      <div class="visual-media">
        {% if is_video %}
          <video controls playsinline preload="metadata"{% if p != "" %} poster="{{ p }}"{% endif %}>
            <source src="{{ m }}"{% if mime != "" %} type="{{ mime }}"{% endif %}>
            Your browser does not support the video tag.
          </video>
        {% else %}
          <img src="{{ m }}" alt="{{ visual.alt | default: visual.title | escape }}" loading="lazy">
        {% endif %}
      </div>
      {% endif %}
 
      <div class="visual-body">
        <div>
          {% if visual.category %}<span style="font-size: 0.75rem; font-weight: 700; color: #009639; text-transform: uppercase;">{{ visual.category }}</span>{% endif %}
          <h3 style="margin: 0.3rem 0 0.5rem 0; font-size: 1.15rem;">{{ visual.title }}</h3>
          {% if visual.description and visual.description != "" %}<p style="font-size: 0.88rem; color: #4b5563; line-height: 1.5; margin-bottom: 0.75rem;">{{ visual.description }}</p>{% endif %}
          <p class="visual-credit">
            {% if visual.author and visual.author != "" %}By {{ visual.author }} · {% endif %}License: {% if v_license_url != "" %}<a href="{{ v_license_url }}" target="_blank" rel="noopener noreferrer">{{ v_license }}</a>{% else %}{{ v_license }}{% endif %}
          </p>
        </div>
 
        {% if visual.citation and visual.citation != "" %}
        <div style="font-size: 0.8rem; color: #6b7280; background: #f3f4f6; padding: 0.5rem 0.75rem; border-radius: 4px; margin-top: 0.5rem;">
          <strong>Cite:</strong> <em>{{ visual.citation }}</em>
        </div>
        {% endif %}
      </div>
 
      {% if visual.language or c != "" %}
      <div class="code-drawer">
        <span style="font-weight: 600; color: #374151;">{% if visual.language %}<i class="fas fa-code"></i> {{ visual.language }}{% endif %}</span>
        {% if c != "" %}<a href="{{ c }}" target="_blank" rel="noopener noreferrer" style="font-weight: 600; color: #009639; text-decoration: underline;">Get Source Script &rarr;</a>{% endif %}
      </div>
      {% endif %}
    </div>
  {%- endfor %}
  </div>
</section>
{% endif %}
 
 
<div style="background: #f9fafb; border-left: 4px solid #009639; border-radius: 6px; padding: 1.25rem 1.5rem; margin: 2rem 0; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem;">
  <div>
    <h4 style="margin: 0 0 0.3rem 0; font-size: 1.05rem; color: #1f2937;">Have something to share?</h4>
    <p style="margin: 0; font-size: 0.9rem; color: #4b5563;">
      Suggest a learning resource, or submit an educational notebook or simulation animation, through our contact page. We will credit your work and link to your repository.
    </p>
  </div>
  <a href="{{ '/contact/' | relative_url }}" class="btn btn--primary" style="margin: 0; font-size: 0.85rem;">
    Contribute or Suggest &rarr;
  </a>
</div>
 
<!-- Learning Library: search + filters -->
<script>
  (function () {
    var cards = Array.prototype.slice.call(document.querySelectorAll(".lib-card"));
    if (!cards.length) return;
    var search   = document.getElementById("lib-search-input");
    var selType  = document.getElementById("lib-filter-type");
    var selLevel = document.getElementById("lib-filter-level");
    var selLang  = document.getElementById("lib-filter-lang");
    var chips    = Array.prototype.slice.call(document.querySelectorAll(".res-chip"));
    var status   = document.getElementById("lib-status");
    var emptyMsg = document.getElementById("lib-empty");
    var clearBtn = document.getElementById("lib-clear");
    var topic = "all";
    // Lower-case and strip accents so "turbulencia" / "Poincaré" match naturally
    function norm(s) {
      s = (s || "").toString().toLowerCase();
      return s.normalize ? s.normalize("NFD").replace(/[\u0300-\u036f]/g, "") : s;
    }
    function val(sel) { return sel ? sel.value : ""; }
    var index = cards.map(function (c) {
      return {
        el: c,
        text: norm(c.getAttribute("data-search")),
        type: c.getAttribute("data-type"),
        level: c.getAttribute("data-level"),
        lang: c.getAttribute("data-lang"),
        topics: (c.getAttribute("data-topics") || "").split("|").filter(Boolean)
      };
    });
    // Total number of resources per topic (shown on the chips)
    chips.forEach(function (chip) {
      var t = chip.getAttribute("data-topic");
      var n = t === "all" ? index.length : index.filter(function (i) { return i.topics.indexOf(t) !== -1; }).length;
      var span = chip.querySelector(".res-count");
      if (span) span.textContent = "(" + n + ")";
    });
    function apply() {
      var words = norm(search.value).trim().split(/\s+/).filter(Boolean);
      var shown = 0;
      index.forEach(function (i) {
        var ok =
          (topic === "all" || i.topics.indexOf(topic) !== -1) &&
          (!val(selType)  || i.type  === val(selType)) &&
          (!val(selLevel) || i.level === val(selLevel)) &&
          (!val(selLang)  || i.lang  === val(selLang)) &&
          words.every(function (w) { return i.text.indexOf(w) !== -1; });
        i.el.classList.toggle("is-hidden", !ok);
        if (ok) shown++;
      });
      status.textContent = "Showing " + shown + " of " + index.length + " resources";
      emptyMsg.hidden = shown !== 0;
      var active = topic !== "all" || val(selType) || val(selLevel) || val(selLang) || words.length;
      clearBtn.hidden = !active;
    }
    chips.forEach(function (chip) {
      chip.addEventListener("click", function () {
        chips.forEach(function (c) {
          c.classList.remove("active");
          c.setAttribute("aria-pressed", "false");
        });
        chip.classList.add("active");
        chip.setAttribute("aria-pressed", "true");
        topic = chip.getAttribute("data-topic");
        apply();
      });
    });
    search.addEventListener("input", apply);
    [selType, selLevel, selLang].forEach(function (s) { if (s) s.addEventListener("change", apply); });
    clearBtn.addEventListener("click", function () {
      search.value = "";
      [selType, selLevel, selLang].forEach(function (s) { if (s) s.value = ""; });
      chips[0].click();   // back to "All topics" (also re-applies)
      search.focus();
    });
    apply();
  })();
</script>
 
