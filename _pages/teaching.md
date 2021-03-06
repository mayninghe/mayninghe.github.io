---
layout: page
permalink: /teaching/
title: Teaching
description: Here are lectures and presentations I developed related to neuroscience, proprioception, psychophysics experimental design, and statistical methods.
nav: true

---


<div class="teaching grid">

  {% assign sorted_teaching = site.teaching | sort: "importance" %}
  {% for teach in sorted_teaching %}
  <div class="grid-item">
    {% if teach.redirect %}
    <a href="{{ teach.redirect }}" target="_blank">
    {% else %}
    <a href="{{ teach.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if teach.img %}
        <img src="{{ teach.img | relative_url }}" alt="teach thumbnail">
        {% endif %}
        <div class="card-body">
          <h4 class="card-title" style="color:black">{{ teach.title }}</h4>
          <p class="card-text">{{ teach.description }}</p>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
