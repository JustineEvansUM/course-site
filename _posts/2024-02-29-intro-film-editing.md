---
title: Intro to Animation
permalink: /intro-film-editing/
author_staff_member: Justine
date: 2024-02-29
featured_image: https://images.pexels.com/photos/262272/pexels-photo-262272.jpeg
percent_complete: 10%;
---


<div class="posts">
  {% for post in site.posts %}
  <div class="post">
    <div class="image" style="background-image: url({{ post.featured_image}})"></div>
    <div class="post-content">
      <!--<p class="date">{{ post.date | date: '%B %d, %Y' }}</p>-->
      <h3>{{ post.title }}</h3>
      <div class="progress-bar">
        <div class="percent-complete" style="width: {{ post.percent_complete }}"></div>
      </div>
      {% if post.content contains "<!-- more -->" %}
      {{ post.content | split:"<!-- more -->" | first }}
      <div style="text-align:right;">
        <a href="{{ post.url }}" style="color:#333;"><i class="fas fa-arrow-right"></i> Read More </a>
      </div>
      {% else %}
      {{ post.content }}
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>
