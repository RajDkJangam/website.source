---
layout: default
permalink: /about/team
title: Team behind the Scene
published: false
---

# Team behind the Scene

<div class="ui four column stackable grid">
  {% for thisAuthor in site.data.team limit:2 %}
  <div class="column">
    <div class="ui fluid card">
      <div class="image">
        <img src="{{ thisAuthor.email | to_gravatar }}" alt="Photo of {{ thisAuthor.name }}">
      </div>
      <div class="content">
        <div class="header">{{ thisAuthor.name }}</div>
        <div class="meta">
          <span class="date">{{ thisAuthor.desig}}</span>
        </div>
        <div class="description">
          {{ thisAuthor.bio | truncatewords: 15 }}
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

<div class="ui divider"></div>
<div class="ui four column stackable grid">

  {% for thisAuthor in site.data.team offset:2 %}
  <div class="column">
    <div class="ui fluid card">
      <div class="image">
        <img src="{{ thisAuthor.email | to_gravatar }}" alt="Photo of {{ thisAuthor.name }}">
      </div>
      <div class="content">
        <div class="header">{{ thisAuthor.name }}</div>
        <div class="meta">
          <span class="date">{{ thisAuthor.desig}}</span>
        </div>
        <div class="description">
          {{ thisAuthor.bio | truncatewords: 15 }}
        </div>
      </div>
    </div>
  </div>
  {% endfor %}


</div>
