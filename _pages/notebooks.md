---
layout: page
title: Notebooks
permalink: /notebooks/
nav: true
nav_order: 4
---

{% assign notebooks = site.notebooks | sort: "date" | reverse %}
<div class="cards">
  {% for nb in notebooks %}
    <a class="card" href="{{ nb.external_url }}" target="_blank" rel="noopener">
      <div class="card-body">
        <div class="card-title">{{ nb.title }}</div>
        <div class="card-desc">{{ nb.description }}</div>
        {% if nb.tags %}
          <div class="card-tags">
            {% for t in nb.tags limit:5 %}
              <span class="tag">{{ t }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
    </a>
  {% endfor %}
</div>