---
title: Teaching
collection: teaching
layout: archive
permalink: /teaching/
---



<h2>Teaching</h2>

{% assign teachings_by_year = site.data.teaching %}

{% for year in teachings_by_year %}
  <h2>{{ year[0] }}</h2>
  <div class="teachinggrid">
    {% for teaching in year[1] %}
      <div class="teachingtile">
        <div class="teachingimage">
          {% if teaching.image %}
            <img src="{{ teaching.image }}" alt="{{ teaching.title }}">
          {% endif %}
        </div>
        <div class="teachingcontent">
          <h3>{{ teaching.title }}</h3>
          <p><strong>Author(s):</strong> {{ teaching.author }}</p>
          {% if teaching.journal %}
            <p><strong>Journal:</strong> {{ teaching.journal }}</p>
          {% endif %}
          {% if teaching.conference %}
            <p><strong>Conference:</strong> {{ teaching.conference }}</p>
          {% endif %}
          <a href="{{ teaching.link }}" class="teachinglink">Read more</a>
        </div>
      </div>
    {% endfor %}
  </div>
{% endfor %}


