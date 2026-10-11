---
title: "Talks & Seminars"
layout: single
permalink: /talks/
classes: wide
author_profile: false
---

<style>
  /* Filter Container */
  .filter-wrapper {
    margin: 1.25rem 0 1.75rem 0;
    padding-bottom: 1.25rem;
    border-bottom: 1px solid #e5e7eb;
  }

  .primary-filters {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.5rem;
  }

  /* Base Filter Button */
  .filter-btn {
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
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
  }

  .filter-btn:hover {
    border-color: #009639;
    color: #009639;
  }

  .filter-btn.active {
    background-color: #009639;
    border-color: #009639;
    color: #ffffff;
    box-shadow: 0 2px 4px rgba(0, 150, 57, 0.2);
  }

  /* Tag Drawer Toggle */
  .btn--toggle-tags {
    border-style: dashed;
    background-color: #f9fafb;
  }
  .btn--toggle-tags.open {
    background-color: #e5e7eb;
    border-color: #9ca3af;
    color: #111827;
  }

  /* Sort Toggle Button */
  .btn--sort {
    margin-left: auto;
    background-color: #f3f4f6;
    border-color: #d1d5db;
  }
  .btn--sort:hover {
    background-color: #e5e7eb;
    border-color: #9ca3af;
    color: #111827;
  }

  /* Clear Button */
  .btn--clear {
    display: none;
    background-color: #fee2e2;
    border-color: #fca5a5;
    color: #b91c1c;
    font-size: 0.8rem;
    padding: 0.3rem 0.75rem;
  }
  .btn--clear:hover {
    background-color: #fecaca;
    color: #991b1b;
  }
  .btn--clear.visible {
    display: inline-flex;
  }

  /* View Switcher (List vs Grid) */
  .view-switcher {
    display: inline-flex;
    border: 1px solid #d1d5db;
    border-radius: 9999px;
    background-color: #ffffff;
    padding: 2px;
  }

  .btn--view {
    appearance: none;
    border: none;
    background: transparent;
    color: #6b7280;
    font-size: 0.78rem;
    font-weight: 600;
    padding: 0.25rem 0.65rem;
    border-radius: 9999px;
    cursor: pointer;
    transition: all 0.15s ease-in-out;
    display: inline-flex;
    align-items: center;
    gap: 0.3rem;
  }

  .btn--view.active {
    background-color: #009639;
    color: #ffffff;
  }

  /* Expandable Tag Drawer */
  .tag-drawer {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.25s cubic-bezier(0.4, 0, 0.2, 1), opacity 0.2s ease, margin 0.2s ease;
    opacity: 0;
    margin-top: 0;
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    align-items: center;
    background: #f8f9fa;
    padding: 0 1rem;
    border-radius: 8px;
  }

  .tag-drawer.is-open {
    max-height: 220px;
    opacity: 1;
    margin-top: 0.75rem;
    padding: 0.75rem 1rem;
    border: 1px solid #e5e7eb;
  }

  .tag-pill {
    appearance: none;
    border: 1px solid #d1d5db;
    background: #ffffff;
    color: #4b5563;
    font-size: 0.78rem;
    font-weight: 500;
    padding: 0.25rem 0.65rem;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.15s ease;
    user-select: none;
  }

  .tag-pill:hover {
    border-color: #009639;
    color: #009639;
  }

  .tag-pill.active {
    background-color: #009639;
    border-color: #009639;
    color: #ffffff;
  }

  .tag-pill .tag-check {
    display: none;
    margin-left: 0.25rem;
  }
  .tag-pill.active .tag-check {
    display: inline;
  }

  /* Status Badges */
  .status-badge {
    display: inline-block;
    font-size: 0.7rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    padding: 0.15rem 0.5rem;
    border-radius: 4px;
    margin-bottom: 0.35rem;
  }
  .status-badge--upcoming {
    background-color: #f2b200;
    color: #ffffff;
  }
  .status-badge--recorded {
    background-color: #e5e7eb;
    color: #4b5563;
  }

  /* Compact Post Card Tags */
  .post-tag {
    display: inline-block;
    font-size: 0.72rem;
    background-color: #f3f4f6;
    color: #4b5563;
    padding: 0.1rem 0.45rem;
    border-radius: 4px;
    margin-right: 0.3rem;
  }

  .talk-card-title {
    margin: 0 0 0.35rem 0;
    font-size: 1.25rem;
    line-height: 1.35;
  }

  .talk-card-title a {
    color: #009639;
    text-decoration: none;
  }
  .talk-card-title a:hover {
    text-decoration: underline;
  }

  .talk-card-meta {
    font-size: 0.88rem;
    color: #4b5563;
    margin-bottom: 0.4rem;
    line-height: 1.4;
  }

  .talk-card.is-hidden {
    display: none !important;
  }

  #no-talks-message {
    display: none;
    text-align: center;
    padding: 2.5rem 1rem;
    color: #6b7280;
    font-size: 1rem;
  }

  /* =========================================================================
     LIST VIEW (Default)
     ========================================================================= */
  #talks-list.view--list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    width: 100%;
  }

  #talks-list.view--list .talk-card {
    display: flex;
    flex-wrap: wrap;
    gap: 1.25rem;
    align-items: center;
    border-bottom: 1px solid #f0f0f0;
    padding-bottom: 1.25rem;
    width: 100%;
    transition: opacity 0.2s ease;
  }

  #talks-list.view--list .talk-card-media {
    flex: 0 0 350px;
    max-width: 100%;
    min-width: 280px;
  }

  #talks-list.view--list .talk-card-media img {
    width: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 14px rgba(0,0,0,0.12);
    object-fit: cover;
    aspect-ratio: 16/9;
    display: block;
  }

  #talks-list.view--list .talk-card-body {
    flex: 1 1 380px;
  }

  /* =========================================================================
     GRID VIEW
     ========================================================================= */
  #talks-list.view--grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 1.75rem;
    width: 100%;
  }

  #talks-list.view--grid .talk-card {
    display: flex;
    flex-direction: column;
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 10px;
    overflow: hidden;
    padding: 0;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  #talks-list.view--grid .talk-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 18px rgba(0, 0, 0, 0.08);
  }

  #talks-list.view--grid .talk-card-media {
    width: 100%;
    flex: none;
    max-width: none;
    min-width: 0;
  }

  #talks-list.view--grid .talk-card-media img {
    width: 100%;
    border-radius: 0;
    box-shadow: none;
    object-fit: cover;
    aspect-ratio: 16/9;
    display: block;
  }

  #talks-list.view--grid .talk-card-body {
    padding: 1.25rem;
    display: flex;
    flex-direction: column;
    flex: 1;
    justify-content: space-between;
  }
</style>

Explore recordings and register for upcoming seminars organized by *Fusion EP Talks*.

<div class="filter-wrapper">
  <!-- Primary Filter Bar -->
  <div class="primary-filters">
    <button class="filter-btn active" id="btn-all" data-status="all">All Talks</button>
    <button class="filter-btn" data-status="upcoming">🟢 Upcoming</button>
    <button class="filter-btn" data-status="recorded">Recorded</button>

    <!-- Expand / Collapse Tag Drawer -->
    <button class="filter-btn btn--toggle-tags" id="toggle-tags-btn" type="button">
      <span>🏷️ Topics</span>
      <span id="toggle-indicator">▾</span>
      <span id="active-tag-count" style="display:none; background:#009639; color:#fff; font-size:0.68rem; border-radius:9999px; padding:0.05rem 0.4rem; margin-left:0.2rem;">0</span>
    </button>

    <!-- Reset / Clear -->
    <button class="filter-btn btn--clear" id="btn-clear" type="button">
      ✕ Clear
    </button>

    <!-- Ascending / Descending Date Sorter -->
    <button class="filter-btn btn--sort" id="btn-sort" type="button" data-order="desc">
      <span>Date:</span> <strong id="sort-label">⇣ Newest first</strong>
    </button>

    <!-- View Mode Switcher -->
    <div class="view-switcher">
      <button class="btn--view active" id="btn-view-list" type="button" title="List View">
        ☰ List
      </button>
      <button class="btn--view" id="btn-view-grid" type="button" title="Grid View">
        ⊞ Grid
      </button>
    </div>
  </div>

  <!-- Expandable Tag Drawer -->
  <div class="tag-drawer" id="tag-drawer">
    <span style="font-size:0.78rem; font-weight:600; color:#6b7280; margin-right:0.4rem;">Filter:</span>
    <button class="tag-pill" data-tag="tokamaks">Tokamaks <span class="tag-check">✓</span></button>
    <button class="tag-pill" data-tag="stellarators">Stellarators <span class="tag-check">✓</span></button>
    <button class="tag-pill" data-tag="turbulence">Turbulence & Transport <span class="tag-check">✓</span></button>
    <button class="tag-pill" data-tag="mhd">MHD & Stability <span class="tag-check">✓</span></button>
    <button class="tag-pill" data-tag="diagnostics">Diagnostics <span class="tag-check">✓</span></button>
    <button class="tag-pill" data-tag="theory">Theory & Modeling <span class="tag-check">✓</span></button>
    <button class="tag-pill" data-tag="simulation">Simulation <span class="tag-check">✓</span></button>
  </div>
</div>

<!-- Empty Result Notice -->
<div id="no-talks-message">
  <p>No seminars match all selected criteria.</p>
</div>

<!-- List of Talks (Defaults to List View) -->
<div id="talks-list" class="view--list">
{% for post in site.posts %}

  {% assign is_recorded = false %}
  {% if post.youtube_id %}
    {% assign is_recorded = true %}
  {% endif %}

  {% capture post_tags %}{% for tag in post.tags %}{{ tag | downcase }} {% endfor %}{% endcapture %}

  <div class="talk-card" 
       data-status="{% if is_recorded %}recorded{% else %}upcoming{% endif %}" 
       data-tags="{{ post_tags | strip }}"
       data-date="{{ post.date | date: "%Y%m%d" }}">
    
    <!-- Thumbnail Poster -->
    {% if post.header.teaser %}
      <div class="talk-card-media">
        <a href="{{ post.url | relative_url }}">
          <img src="{{ post.header.teaser | relative_url }}" 
               alt="{{ post.title }}">
        </a>
      </div>
    {% endif %}

    <!-- Card Details -->
    <div class="talk-card-body">
      <div>
        {% if is_recorded %}
          <span class="status-badge status-badge--recorded">Recorded</span>
        {% else %}
          <span class="status-badge status-badge--upcoming">Upcoming</span>
        {% endif %}

        <h2 class="talk-card-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        
        <!-- Primary Metadata Line -->
        <p class="talk-card-meta">
          📅 {{ post.date | date: "%B %d, %Y" }}
          {% if post.speaker %}
            &nbsp;|&nbsp; 👤 <strong>{{ post.speaker }}</strong>
          {% endif %}
          {% if post.affiliation %}
            <span style="color: #6b7280;">({{ post.affiliation }})</span>
          {% endif %}
        </p>

        <!-- Topic Tags -->
        {% if post.tags and post.tags.size > 0 %}
          <div style="margin-bottom: 0.65rem;">
            {% for tag in post.tags %}
              <span class="post-tag">#{{ tag }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>

      <!-- Action Button -->
      <div>
        {% if is_recorded %}
          <a href="{{ post.url | relative_url }}" class="btn btn--primary" style="margin: 0; font-size: 0.8rem; padding: 0.35rem 0.8rem;">
            View Details & Recording
          </a>
        {% else %}
          <a href="{{ post.url | relative_url }}" class="btn btn--warning" style="margin: 0; font-size: 0.8rem; padding: 0.35rem 0.8rem;">
            Register & Details
          </a>
        {% endif %}
      </div>

    </div>
  </div>
{% endfor %}
</div>

<!-- Sorter, View Switcher, Multi-Select & Drawer Logic -->
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const toggleBtn = document.getElementById("toggle-tags-btn");
    const toggleIndicator = document.getElementById("toggle-indicator");
    const tagDrawer = document.getElementById("tag-drawer");
    const tagCountBadge = document.getElementById("active-tag-count");
    const clearBtn = document.getElementById("btn-clear");
    const btnAll = document.getElementById("btn-all");
    const sortBtn = document.getElementById("btn-sort");
    const sortLabel = document.getElementById("sort-label");

    const btnList = document.getElementById("btn-view-list");
    const btnGrid = document.getElementById("btn-view-grid");
    const talksContainer = document.getElementById("talks-list");

    const statusButtons = document.querySelectorAll("[data-status]");
    const tagPills = document.querySelectorAll(".tag-pill");
    let talkCards = Array.from(document.querySelectorAll(".talk-card"));
    const noResultsMsg = document.getElementById("no-talks-message");

    let currentStatus = "all";
    let activeTags = new Set();
    let sortOrder = "desc";

    // 1. View Switcher (List vs Grid) with LocalStorage persistence
    const savedView = localStorage.getItem("talks_view_mode") || "list";
    setViewMode(savedView);

    btnList.addEventListener("click", () => setViewMode("list"));
    btnGrid.addEventListener("click", () => setViewMode("grid"));

    function setViewMode(mode) {
      if (mode === "grid") {
        talksContainer.classList.remove("view--list");
        talksContainer.classList.add("view--grid");
        btnGrid.classList.add("active");
        btnList.classList.remove("active");
        localStorage.setItem("talks_view_mode", "grid");
      } else {
        talksContainer.classList.remove("view--grid");
        talksContainer.classList.add("view--list");
        btnList.classList.add("active");
        btnGrid.classList.remove("active");
        localStorage.setItem("talks_view_mode", "list");
      }
    }

    // 2. Toggle Drawer
    toggleBtn.addEventListener("click", function () {
      const isOpen = tagDrawer.classList.toggle("is-open");
      toggleBtn.classList.toggle("open", isOpen);
      toggleIndicator.textContent = isOpen ? "▴" : "▾";
    });

    // 3. Status Filters
    statusButtons.forEach(btn => {
      btn.addEventListener("click", function () {
        const selected = this.getAttribute("data-status");

        if (selected === "all") {
          resetAllFilters();
          return;
        }

        statusButtons.forEach(b => b.classList.remove("active"));
        this.classList.add("active");
        currentStatus = selected;
        btnAll.classList.remove("active");

        applyFilters();
      });
    });

    // 4. Multi-Select Tags
    tagPills.forEach(pill => {
      pill.addEventListener("click", function () {
        const tag = this.getAttribute("data-tag").toLowerCase();

        if (activeTags.has(tag)) {
          activeTags.delete(tag);
          this.classList.remove("active");
        } else {
          activeTags.add(tag);
          this.classList.add("active");
        }

        btnAll.classList.remove("active");
        updateDrawerBadge();
        applyFilters();
      });
    });

    // 5. Date Sorting
    sortBtn.addEventListener("click", function () {
      sortOrder = (sortOrder === "desc") ? "asc" : "desc";
      sortBtn.setAttribute("data-order", sortOrder);
      sortLabel.textContent = (sortOrder === "desc") ? "⇣ Newest first" : "⇡ Oldest first";
      sortCards();
    });

    function sortCards() {
      talkCards.sort((a, b) => {
        const dateA = parseInt(a.getAttribute("data-date") || "0", 10);
        const dateB = parseInt(b.getAttribute("data-date") || "0", 10);
        return (sortOrder === "desc") ? (dateB - dateA) : (dateA - dateB);
      });

      talkCards.forEach(card => talksContainer.appendChild(card));
    }

    // 6. Clear Filters
    clearBtn.addEventListener("click", resetAllFilters);

    function resetAllFilters() {
      currentStatus = "all";
      activeTags.clear();

      statusButtons.forEach(b => b.classList.remove("active"));
      btnAll.classList.add("active");
      tagPills.forEach(p => p.classList.remove("active"));

      if (tagDrawer.classList.contains("is-open")) {
        tagDrawer.classList.remove("is-open");
        toggleBtn.classList.remove("open");
        toggleIndicator.textContent = "▾";
      }

      updateDrawerBadge();
      applyFilters();
    }

    function updateDrawerBadge() {
      const count = activeTags.size;
      if (count > 0) {
        tagCountBadge.textContent = count;
        tagCountBadge.style.display = "inline";
      } else {
        tagCountBadge.style.display = "none";
      }
    }

    // 7. Apply Filter Visibility
    function applyFilters() {
      let visibleCount = 0;
      const isFiltered = currentStatus !== "all" || activeTags.size > 0;

      if (isFiltered) {
        clearBtn.classList.add("visible");
      } else {
        clearBtn.classList.remove("visible");
      }

      talkCards.forEach(card => {
        const cardStatus = card.getAttribute("data-status") || "";
        const rawCardTags = (card.getAttribute("data-tags") || "").split(" ").filter(Boolean);

        const matchesStatus = (currentStatus === "all" || cardStatus === currentStatus);

        let matchesTags = true;
        activeTags.forEach(tag => {
          if (!rawCardTags.includes(tag)) {
            matchesTags = false;
          }
        });

        if (matchesStatus && matchesTags) {
          card.classList.remove("is-hidden");
          visibleCount++;
        } else {
          card.classList.add("is-hidden");
        }
      });

      noResultsMsg.style.display = visibleCount === 0 ? "block" : "none";
    }

    // 8. BFCache Fix
    window.addEventListener("pageshow", function (event) {
      if (event.persisted) {
        resetAllFilters();
      }
    });
  });
</script>
