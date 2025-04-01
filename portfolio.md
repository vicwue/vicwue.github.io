---
layout: page
title: Portfolio
permalink: /portfolio/
---



Jump to: {% for tag in site.tags %} <a href="#{{tag[0]}}" class="categorypill">{{ tag[0] }}</a> {% endfor %}

{% for tag in site.tags %}
  <span class="categorypill" id="{{tag[0]}}">{{ tag[0] }}</span>
  <div class="listofcards">
    {% for post in tag[1] %}
      <div class="card project" onClick="window.location.replace('{{ post.url }}')">
        <h4>{{ post.title }}</h4>
        <span class="role">{{ post.role }} </span><span class="role"> {{ post.company }} </span> <span class="role"> {{ post.location }} </span>

        <img src="{{ post.thumbnail }}" />
        <div class="excerpt">      {{ post.excerpt }}</div>
      </div>

    {% endfor %}
  </div>
  
{% endfor %}

