---
layout: page
title: Portfolio
nav-menu: true
description: My portfolio of work
image: null
author: null
show_tile: false
---

Welcome to my portfolio. Below are highlighted collections of work from 2025 — each page includes a slideshow of sketches and finished studies.

<div class="portfolio-grid">
  {% assign items = site.pages | where: "portfolio_item", true | sort: "title" %}
  {% for item in items %}
  <article class="portfolio-card">
    <a class="image" href="{{ item.url | relative_url }}">
      <img src="{{ item.image | relative_url }}" alt="{{ item.title }}" />
    </a>
    <div class="portfolio-card-body">
      <h2><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
      <p>{{ item.portfolio_description }}</p>
      <ul class="actions">
        <li><a class="button primary small" href="{{ item.url | relative_url }}">View slideshow</a></li>
      </ul>
    </div>
  </article>
  {% endfor %}
</div>