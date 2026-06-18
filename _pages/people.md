---
title: ICR Team Members
permalink: /people/
layout: archive
author_profile: false
---

{% assign people = site.people | sort: "order" %}

<div class="people-grid">
{% for person in people %}
  <div class="person-card">

    <img src="{{ person.image }}" alt="{{ person.title }}" class="person-photo">

    <h3>{{ person.title }}</h3>

    <p class="person-role">{{ person.role }}</p>

    <p class="person-description">
      {{ person.description }}
    </p>

    {% if person.social %}
    <div class="person-links">
      {% for item in person.social %}
        <a href="{{ item.link }}" target="_blank">
          <i class="{{ item.icon }}"></i>
        </a>
      {% endfor %}
    </div>
    {% endif %}

  </div>
{% endfor %}
</div>