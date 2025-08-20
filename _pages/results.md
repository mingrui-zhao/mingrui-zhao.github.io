---
layout: page
title: Course Project Results
permalink: /results/
nav: false
sitemap: false
description: Temporary page to showcase video inbetweening results for the course project.
---

<style>
  .results-container {
    display: grid;
    gap: 2rem;
  }
  .result-block {
    border-top: 1px solid var(--global-divider-color, #e5e5e5);
    padding-top: 1.5rem;
  }
  .result-title {
    margin-bottom: 0.75rem;
    font-weight: 600;
    text-align: left;
  }
  .t-block {
    display: grid;
    grid-template-rows: auto auto auto;
    align-items: center;
    justify-items: center;
    gap: 0.75rem;
    /* scoped variables */
    --gap: 0.75rem;
    max-width: 70%;
    margin: 0 auto;
  }
  .input-image {
    width: calc((100% - (var(--cols, 4) - 1) * var(--gap, 0.75rem)) / var(--cols, 4));
    height: auto;
    border-radius: 6px;
    box-shadow: 0 1px 2px rgba(0,0,0,0.06);
  }
  .video-row {
    display: grid;
    grid-template-columns: repeat(var(--cols, 4), minmax(160px, 1fr));
    gap: var(--gap);
    justify-content: center;
    align-items: center;
    width: 100%;
  }
  .result-video {
    width: 100%;
    height: auto;
    border-radius: 6px;
    box-shadow: 0 1px 2px rgba(0,0,0,0.06);
    background: #000;
  }
  .video-caption {
    text-align: center;
    font-size: 0.85rem;
    margin-top: 0.25rem;
    color: var(--global-text-color-secondary, #666);
  }
  .video-item { display: flex; flex-direction: column; align-items: center; }

  @media (max-width: 768px) {
    .video-row { grid-template-columns: repeat(var(--cols, 4), minmax(120px, 1fr)); }
  }
</style>

<div class="results-container">
  {% assign all_files = site.static_files %}
  {% for file in all_files %}
    {% if file.path contains '/assets/results/' and file.path contains '/start.png' %}
      {% assign dir = file.path | remove: '/start.png' %}
      {% assign folder = dir | split: '/' | last %}

      {% assign start_img = dir | append: '/start.png' %}
      {% assign end_img = dir | append: '/end.png' %}

      {% assign wan_mp4 = dir | append: '/WAN.mp4' %}
      {% assign vace_mp4 = dir | append: '/VACE.mp4' %}
      {% assign end_mp4 = dir | append: '/end.mp4' %}
      {% assign mid_mp4 = dir | append: '/mid_interpolation.mp4' %}

      {% assign wan_exists = all_files | where: 'path', wan_mp4 %}
      {% assign vace_exists = all_files | where: 'path', vace_mp4 %}
      {% assign end_exists = all_files | where: 'path', end_mp4 %}
      {% assign mid_exists = all_files | where: 'path', mid_mp4 %}

      {% assign num_videos = 0 %}
      {% if wan_exists and wan_exists.size > 0 %}{% assign num_videos = num_videos | plus: 1 %}{% endif %}
      {% if vace_exists and vace_exists.size > 0 %}{% assign num_videos = num_videos | plus: 1 %}{% endif %}
      {% if end_exists and end_exists.size > 0 %}{% assign num_videos = num_videos | plus: 1 %}{% endif %}
      {% if mid_exists and mid_exists.size > 0 %}{% assign num_videos = num_videos | plus: 1 %}{% endif %}

      <section class="result-block" id="{{ folder }}">
        <div class="result-title">{{ folder | replace: '_', ' ' | capitalize }}</div>
        <div class="t-block" style="{% if num_videos > 0 %}--cols: {{ num_videos }};{% endif %}">
          <img class="input-image" src="{{ start_img | relative_url }}" alt="{{ folder }} start" loading="eager" />

          {% if num_videos > 0 %}
          <div class="video-row">
            {% if wan_exists and wan_exists.size > 0 %}
              <div class="video-item">
                <video class="result-video" controls loop muted playsinline>
                  <source src="{{ wan_mp4 | relative_url }}" type="video/mp4" />
                </video>
                <div class="video-caption">WAN</div>
              </div>
            {% endif %}
            {% if vace_exists and vace_exists.size > 0 %}
              <div class="video-item">
                <video class="result-video" controls loop muted playsinline>
                  <source src="{{ vace_mp4 | relative_url }}" type="video/mp4" />
                </video>
                <div class="video-caption">VACE</div>
              </div>
            {% endif %}
            {% if end_exists and end_exists.size > 0 %}
              <div class="video-item">
                <video class="result-video" controls loop muted playsinline>
                  <source src="{{ end_mp4 | relative_url }}" type="video/mp4" />
                </video>
                <div class="video-caption">End (video)</div>
              </div>
            {% endif %}
            {% if mid_exists and mid_exists.size > 0 %}
              <div class="video-item">
                <video class="result-video" controls loop muted playsinline>
                  <source src="{{ mid_mp4 | relative_url }}" type="video/mp4" />
                </video>
                <div class="video-caption">Mid interpolation</div>
              </div>
            {% endif %}
          </div>
          {% endif %}

          <img class="input-image" src="{{ end_img | relative_url }}" alt="{{ folder }} end" loading="lazy" />
        </div>
      </section>
    {% endif %}
  {% endfor %}
</div>



