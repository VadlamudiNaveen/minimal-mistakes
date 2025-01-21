---
collection: People
permalink: /people/
layout: archive
---

<h2>Our Team</h2>
<h1>Faculty</h1>
<div class="team-container">
  {% for person in site.data.faculty %}
  <div class="tile-card">
    <div class="card-image">
      <img src="{{ person.image }}" alt="{{ person.name }}">
    </div>
    <div class="card-content">
      <h2 class="card-title">{{ person.name }}</h2>
      <p class="card-role">{{ person.role }}</p>
      <p class="card-description">{{ person.description }}</p>
      {% if person.link %}
      <a href="{{ person.link }}" class="card-link">Learn More</a>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

<div class="team-container">
  <h1>Graduate Students</h1>
  <div class="graduate-container">
    {% for person in site.data.graduate %}
      <div class="graduate-tile-card">
        <div class="graduate-card-image">
          <img src="{{ person.image }}" alt="{{ person.name }}">
        </div>
        <div class="graduate-card-content">
          <h2 class="graduate-card-title">{{ person.name }}</h2>
          <p class="graduate-card-role">{{ person.role }}</p>
          <p class="graduate-card-description">{{ person.description }}</p>
          {% if person.link %}
            <a href="{{ person.link }}" class="graduate-card-link">Learn More</a>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>



