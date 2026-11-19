---
title: "Opportunities: Degrees, PhDs, Postdocs, Jobs & Internships"
layout: single
permalink: /opportunities/
classes: wide
author_profile: false
---
 
<style>
  /* Filter bar */
  .opp-filter-bar {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
    margin: 1.5rem 0 2.5rem 0;
    padding-bottom: 1.25rem;
    border-bottom: 1px solid #e5e7eb;
  }
  .opp-filter-btn {
    appearance: none;
    border: 1px solid #d1d5db;
    background-color: #ffffff;
    color: #374151;
    font-size: 0.85rem;
    font-weight: 600;
    padding: 0.45rem 1rem;
    border-radius: 9999px;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
  }
  .opp-filter-btn:hover {
    border-color: #009639;
    color: #009639;
  }
  .opp-filter-btn.active {
    background-color: #009639;
    border-color: #009639;
    color: #ffffff;
    box-shadow: 0 2px 4px rgba(0, 150, 57, 0.2);
  }
  /* Grid of Opportunities */
  .opp-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 1.5rem;
    margin-bottom: 3rem;
  }
  .opp-card {
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
  .opp-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 14px rgba(0,0,0,0.08);
  }
  .opp-card.is-hidden {
    display: none !important;
  }
  /* Track Badges */
  .badge-track {
    display: inline-block;
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    padding: 0.2rem 0.55rem;
    border-radius: 4px;
    margin-bottom: 0.5rem;
  }
  .badge-track--master { background-color: #dbeafe; color: #1e40af; }
  .badge-track--phd { background-color: #dcfce7; color: #15803d; }
  .badge-track--school, .badge-track--internship { background-color: #fef3c7; color: #b45309; }
  /* Deadline indicator */
  .deadline-tag {
    font-size: 0.8rem;
    font-weight: 600;
    color: #b91c1c;
    background: #fee2e2;
    padding: 0.2rem 0.6rem;
    border-radius: 4px;
    display: inline-flex;
    align-items: center;
    gap: 0.3rem;
  }
  .deadline-tag--ongoing {
    color: #047857;
    background: #d1fae5;
  }
  /* Submission callout */
  .submit-callout {
    background: #f9fafb;
    border-left: 4px solid #009639;
    border-radius: 6px;
    padding: 1.25rem 1.5rem;
    margin: 2rem 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
  }
  /* ------------------------------------------------------------------
     ADDITIONS (existing rules above are untouched)
     ------------------------------------------------------------------ */
  /* New / split badges */
  .badge-track--internship { background-color: #ffedd5; color: #c2410c; }
  .badge-track--postdoc    { background-color: #ccfbf1; color: #0f766e; }
  .badge-track--job        { background-color: #ede9fe; color: #6d28d9; }
  .badge-track--other      { background-color: #f3f4f6; color: #374151; }
  /* New deadline states */
  .deadline-tag--soon        { color: #ffffff; background: #b91c1c; }
  .deadline-tag--orientative { color: #3730a3; background: #e0e7ff; }
  .deadline-tag--tba         { color: #1e40af; background: #dbeafe; }
  .deadline-tag--check       { color: #92400e; background: #fef3c7; }
  /* Filter counts */
  .opp-count { font-weight: 500; opacity: 0.75; margin-left: 0.2rem; }
  /* Empty-state message */
  .opp-empty {
    padding: 1.5rem;
    margin-bottom: 3rem;
    text-align: center;
    color: #6b7280;
    background: #f9fafb;
    border: 1px dashed #d1d5db;
    border-radius: 8px;
  }
  /* Screen-reader-only text */
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
 
Discover academic and professional pathways in nuclear fusion and plasma physics, including European master's degrees, funded PhD and postdoc vacancies, summer schools, internships, and jobs in industry.
 
<div class="submit-callout">
  <div>
    <h4 style="margin: 0 0 0.3rem 0; font-size: 1.05rem; color: #1f2937;">Are you recruiting students or researchers?</h4>
    <p style="margin: 0; font-size: 0.9rem; color: #4b5563;">
      Post your Master's, PhD or postdoc vacancy, job, internship or summer school announcement directly to our community board.
    </p>
  </div>
  <a href="{{ '/contact/' | relative_url }}" class="btn btn--primary" style="margin: 0; font-size: 0.85rem;">
    Submit an Opportunity
  </a>
</div>
{% comment %}
==============================================================================
 BUILD STEP (outputs nothing by itself, only prepares variables)
 
 Deadline states, decided per entry:
   0 = date        -> valid "YYYY-MM-DD" (hidden into archive once passed)
   1 = orientative -> approximate text like "Early June", "Mid-February 2027"
                      (optional `sort_date: YYYY-MM-DD` controls sort order)
   2 = ongoing     -> "ongoing" (always active)
   3 = tba         -> "TBA" (always active, "Deadline TBA" tag)
   4 = empty       -> blank/nil (always active, "Check deadline" tag)
 
 Sorting: exact dates (soonest first) -> orientative -> ongoing -> TBA -> empty.
==============================================================================
{% endcomment %}
{%- assign today_int = site.time | date: "%Y%m%d" | plus: 0 -%}
{%- assign today_ts = site.time | date: "%Y-%m-%d" | date: "%s" | plus: 0 -%}
{%- assign soon_days = 14 -%}
 
{%- assign sort_rows = "" | split: "" -%}
{%- for item in site.data.opportunities -%}
  {%- assign dl_raw = item.deadline | append: "" | strip -%}
  {%- assign dl = dl_raw | downcase -%}
  {%- assign dl_int = dl | date: "%Y%m%d" | plus: 0 -%}
  {%- if dl == "" -%}
    {%- assign key = "499999999" -%}
  {%- elsif dl == "ongoing" -%}
    {%- assign key = "200000000" -%}
  {%- elsif dl == "tba" -%}
    {%- assign key = "300000000" -%}
  {%- elsif dl.size == 10 and dl contains "-" and dl_int > 19000000 -%}
    {%- assign key = "0" | append: dl_int -%}
  {%- else -%}
    {%- assign sd = item.sort_date | append: "" | strip -%}
    {%- assign sd_int = sd | date: "%Y%m%d" | plus: 0 -%}
    {%- if sd.size == 10 and sd contains "-" and sd_int > 19000000 -%}
      {%- assign key = "1" | append: sd_int -%}
    {%- else -%}
      {%- assign key = "199999999" -%}
    {%- endif -%}
  {%- endif -%}
  {%- assign idx_pad = forloop.index0 | prepend: "0000" | slice: -4, 4 -%}
  {%- assign row = key | append: "-" | append: idx_pad | append: "~" | append: forloop.index0 -%}
  {%- assign sort_rows = sort_rows | push: row -%}
{%- endfor -%}
{%- assign sorted_rows = sort_rows | sort -%}
 
{%- assign count_all = 0 -%}
{%- assign count_master = 0 -%}
{%- assign count_phd = 0 -%}
{%- assign count_postdoc = 0 -%}
{%- assign count_school = 0 -%}
{%- assign count_job = 0 -%}
{%- assign count_closed = 0 -%}
{%- assign grid_html = "" -%}
{%- assign archive_html = "" -%}
 
{%- for row in sorted_rows -%}
  {%- assign idx = row | split: "~" | last | plus: 0 -%}
  {%- assign item = site.data.opportunities[idx] -%}
  {%- assign group = row | slice: 0 -%}
  {%- assign type = item.type | append: "" | downcase | strip -%}
  {%- assign dl = item.deadline | append: "" | strip -%}
 
  {%- assign is_closed = false -%}
  {%- if group == "0" -%}
    {%- assign row_date_int = row | slice: 1, 8 | plus: 0 -%}
    {%- if row_date_int < today_int -%}
      {%- assign is_closed = true -%}
    {%- endif -%}
  {%- endif -%}
 
  {%- if is_closed -%}
 
    {%- assign count_closed = count_closed | plus: 1 -%}
    {%- capture li -%}
      <li style="margin-bottom: 0.5rem; font-size: 0.9rem; color: #6b7280;"><strong>{{ item.title }}</strong>{% if item.institution %} – {{ item.institution }}{% endif %} (Closed: {{ dl | date: "%B %-d, %Y" }})</li>
    {%- endcapture -%}
    {%- comment -%} Prepend, so the most recently closed appears first {%- endcomment -%}
    {%- capture archive_html -%}{{ li }}{{ archive_html }}{%- endcapture -%}
 
  {%- else -%}
 
    {%- assign count_all = count_all | plus: 1 -%}
    {%- case type -%}
      {%- when "master" -%}{%- assign count_master = count_master | plus: 1 -%}
      {%- when "phd" -%}{%- assign count_phd = count_phd | plus: 1 -%}
      {%- when "postdoc" -%}{%- assign count_postdoc = count_postdoc | plus: 1 -%}
      {%- when "school" or "internship" -%}{%- assign count_school = count_school | plus: 1 -%}
      {%- when "job" -%}{%- assign count_job = count_job | plus: 1 -%}
    {%- endcase -%}
 
    {%- comment -%} Days left (0 = today). Only meaningful for real dates. {%- endcomment -%}
    {%- assign days_left = 9999 -%}
    {%- if group == "0" -%}
      {%- assign item_ts = dl | date: "%s" | plus: 0 -%}
      {%- assign diff_sec = item_ts | minus: today_ts | plus: 43200 -%}
      {%- assign days_left = diff_sec | divided_by: 86400 -%}
    {%- endif -%}
 
    {%- capture card -%}
<div class="opp-card" data-track="{{ type }}"{% if item.posted %} data-posted="{{ item.posted }}"{% endif %}>
  <div>
    <span class="badge-track badge-track--{% case type %}{% when 'master' or 'phd' or 'postdoc' or 'school' or 'internship' or 'job' %}{{ type }}{% else %}other{% endcase %}">
      {%- case type -%}
        {%- when "master" -%}Master's Degree
        {%- when "phd" -%}PhD Position
        {%- when "postdoc" -%}Postdoc Position
        {%- when "school" -%}Summer School / Workshop
        {%- when "internship" -%}Internship / Grant
        {%- when "job" -%}Job / Industry
        {%- else -%}Opportunity
      {%- endcase -%}
    </span>
    <h3 style="margin: 0.4rem 0 0.5rem 0; font-size: 1.2rem; color: #111827;">{{ item.title }}</h3>
 
    {% if item.institution %}<p style="font-size: 0.88rem; color: #4b5563; margin-bottom: 0.4rem;">🏛️ <strong>{{ item.institution }}</strong></p>{% endif %}
    {% if item.location %}<p style="font-size: 0.85rem; color: #6b7280; margin-bottom: 0.9rem;">📍 {{ item.location }}</p>{% endif %}
    {% if item.description and item.description != "" %}<p style="font-size: 0.9rem; color: #374151; line-height: 1.5; margin-bottom: 1rem;">{{ item.description }}</p>{% endif %}
  </div>
  <div>
    <div style="margin-bottom: 1rem;">
      {%- case group -%}
        {%- when "1" -%}
          <span class="deadline-tag deadline-tag--orientative">🗓️ Expected: {{ dl }}</span>
        {%- when "2" -%}
          <span class="deadline-tag deadline-tag--ongoing">📅 Rolling / Ongoing</span>
        {%- when "3" -%}
          <span class="deadline-tag deadline-tag--tba">📅 Deadline TBA</span>
        {%- when "4" -%}
          <span class="deadline-tag deadline-tag--check">⚠️ Check deadline on the official page</span>
        {%- else -%}
          {%- if days_left <= soon_days -%}
            <span class="deadline-tag deadline-tag--soon">⏰ Closing soon: {{ dl | date: "%B %-d, %Y" }}
              {%- if days_left <= 0 %} · today{% elsif days_left == 1 %} · tomorrow{% else %} · in {{ days_left }} days{% endif -%}
            </span>
          {%- else -%}
            <span class="deadline-tag">📅 Deadline: {{ dl | date: "%B %-d, %Y" }}</span>
          {%- endif -%}
      {%- endcase -%}
    </div>
    {% if item.funding and item.funding != "" %}<p style="font-size: 0.82rem; color: #047857; margin-bottom: 1rem; font-weight: 500;">💶 {{ item.funding }}</p>{% endif %}
 
    {% if item.link and item.link != "" %}<a href="{{ item.link }}" target="_blank" rel="noopener noreferrer" class="btn btn--inverse" style="width: 100%; text-align: center; margin: 0;">Official Details & Apply &rarr;</a>{% endif %}
  </div>
</div>
    {%- endcapture -%}
    {%- capture grid_html -%}{{ grid_html }}{{ card }}{%- endcapture -%}
  {%- endif -%}
{%- endfor -%}
 
<!-- Category Filters -->
<div class="opp-filter-bar" role="group" aria-label="Filter opportunities by category">
  <button type="button" class="opp-filter-btn active" data-filter="all" aria-pressed="true">All Tracks <span class="opp-count">({{ count_all }})</span></button>
  <button type="button" class="opp-filter-btn" data-filter="master" aria-pressed="false">🎓 Master's Programmes <span class="opp-count">({{ count_master }})</span></button>
  <button type="button" class="opp-filter-btn" data-filter="phd" aria-pressed="false">🔬 PhD Positions <span class="opp-count">({{ count_phd }})</span></button>
  <button type="button" class="opp-filter-btn" data-filter="postdoc" aria-pressed="false">🧑‍🔬 Postdocs <span class="opp-count">({{ count_postdoc }})</span></button>
  <button type="button" class="opp-filter-btn" data-filter="school" aria-pressed="false">☀️ Summer Schools & Internships <span class="opp-count">({{ count_school }})</span></button>
  <button type="button" class="opp-filter-btn" data-filter="job" aria-pressed="false">💼 Jobs & Industry <span class="opp-count">({{ count_job }})</span></button>
</div>
<h2>Active Calls & Positions</h2>
 
<!-- Announces filter results to screen readers -->
<p id="opp-status" class="sr-only" role="status" aria-live="polite"></p>
{% if count_all == 0 %}
<p class="opp-empty">There are no open opportunities at the moment. Check back soon, or submit one using the button above.</p>
{% endif %}
<p id="opp-empty" class="opp-empty" hidden>No opportunities in this category right now. Check back soon, or submit one using the button above.</p>
<div class="opp-grid" id="opps-container">
{{ grid_html }}
</div>
{% if count_closed > 0 %}
<!-- Collapsible Archive for Expired Calls -->
<details style="margin-top: 3rem; background: #f9fafb; border: 1px solid #e5e7eb; border-radius: 8px; padding: 1rem 1.25rem;">
  <summary style="font-weight: 600; color: #4b5563; cursor: pointer;">
    📁 View Recently Closed / Historical Positions ({{ count_closed }})
  </summary>
  <div style="margin-top: 1rem;">
    <ul>
{{ archive_html }}
    </ul>
  </div>
</details>
{% endif %}
<!-- Track Filtering Script -->
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const filterBtns = document.querySelectorAll(".opp-filter-btn");
    const cards = document.querySelectorAll(".opp-card");
    const emptyMsg = document.getElementById("opp-empty");
    const status = document.getElementById("opp-status");
    // Which card types each filter button shows
    const groups = {
      all: null,                          // everything
      school: ["school", "internship"]    // summer schools & internships share a button
    };
    function matches(filter, track) {
      if (filter === "all") return true;
      const allowed = groups[filter] || [filter];
      return allowed.indexOf(track) !== -1;
    }
    filterBtns.forEach(btn => {
      btn.addEventListener("click", function () {
        filterBtns.forEach(b => {
          b.classList.remove("active");
          b.setAttribute("aria-pressed", "false");
        });
        this.classList.add("active");
        this.setAttribute("aria-pressed", "true");
        const selectedTrack = this.getAttribute("data-filter");
        let visible = 0;
        cards.forEach(card => {
          if (matches(selectedTrack, card.getAttribute("data-track"))) {
            card.classList.remove("is-hidden");
            visible++;
          } else {
            card.classList.add("is-hidden");
          }
        });
        // Empty state (only for filters; the "nothing at all" case is rendered by Liquid)
        if (emptyMsg) emptyMsg.hidden = !(visible === 0 && cards.length > 0);
        // Screen-reader announcement
        if (status) {
          status.textContent = visible + (visible === 1 ? " opportunity shown" : " opportunities shown");
        }
      });
    });
  });
</script>
