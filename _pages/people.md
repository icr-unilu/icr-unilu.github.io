---
title: ICR Team Members
permalink: /people/
layout: splash
author_profile: false
---

{% assign people = site.people | sort: "order" %}

<div class="people-grid">

{% for person in people %}
  <div class="person-card">

    <div class="person-photo-wrapper">

      <img src="{{ person.image }}" alt="{{ person.title }}" class="person-photo">
    
      <div class="person-overlay">
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
    
    </div>

    <h3 class="person-name">{{ person.title }}</h3>

    <p class="person-role">{{ person.role }}</p>

    <p class="person-description">
      {{ person.description }}
    </p>

  </div>
{% endfor %}

</div>