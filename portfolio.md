---
layout: page
title: Portfolio
permalink: /portfolio/
---



Jump to: {% for tag in site.tags %} <a href="#{{tag[0]}}" class="categorypill">{{ tag[0] }}</a> {% endfor %}

{% for tag in site.tags %}
  <span class="categorypill" id="{{tag[0]}}">{{ tag[0] }}</span>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>
            {{ post.excerpt }}
</li>
    {% endfor %}
  </ul>
  <hr>
{% endfor %}

