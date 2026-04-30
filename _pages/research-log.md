---
layout: default
permalink: /research-log/
title: research log
nav: false
nav_order: 9
---

<div class="post">
  <div class="header-bar">
    <h1>Research Log</h1>
    <h2>daily notes, paper summaries, and topic deep-dives</h2>
  </div>

  <br>

  <div class="container featured-posts">
    <div class="row row-cols-1 row-cols-md-3">

      <div class="col mb-4">
        <a href="{{ '/research-log/daily-log/' | relative_url }}">
          <div class="card hoverable h-100">
            <div class="card-body">
              <h3 class="card-title">Daily Log</h3>
              <p class="card-text">Day-by-day notes — what I read, tried, and learned.</p>
              {% assign daily_count = site.research_log | where_exp: "p", "p.categories contains 'daily-log'" | size %}
              <p class="post-meta">{{ daily_count }} entr{% if daily_count == 1 %}y{% else %}ies{% endif %}</p>
            </div>
          </div>
        </a>
      </div>

      <div class="col mb-4">
        <a href="{{ '/research-log/papers/' | relative_url }}">
          <div class="card hoverable h-100">
            <div class="card-body">
              <h3 class="card-title">Papers</h3>
              <p class="card-text">Notes and summaries from papers I have read.</p>
              {% assign papers_count = site.research_log | where_exp: "p", "p.categories contains 'papers'" | size %}
              <p class="post-meta">{{ papers_count }} entr{% if papers_count == 1 %}y{% else %}ies{% endif %}</p>
            </div>
          </div>
        </a>
      </div>

      <div class="col mb-4">
        <a href="{{ '/research-log/topics/' | relative_url }}">
          <div class="card hoverable h-100">
            <div class="card-body">
              <h3 class="card-title">Topics</h3>
              <p class="card-text">Consolidated notes on research topics and concepts.</p>
              {% assign topics_count = site.research_log | where_exp: "p", "p.categories contains 'topics'" | size %}
              <p class="post-meta">{{ topics_count }} entr{% if topics_count == 1 %}y{% else %}ies{% endif %}</p>
            </div>
          </div>
        </a>
      </div>

    </div>
  </div>
</div>
