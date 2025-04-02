---
layout: page
title: Portfolio
permalink: /portfolio/
---



Jump to: {% for tag in site.tags %} <a href="#{{tag[0]}}" class="categorypill {{tag[0]}}">{{ tag[0] }}</a> {% endfor %}

{% for tag in site.tags %}
  {%- if tag[0] != "delivery" -%}
  <span class="categorypill {{tag[0]}}" id="{{tag[0]}}">{{ tag[0] }}</span>
  <div class="listofcards row list-{{tag[0]}}">
    {% for post in tag[1] %}
      <div class="col-12 col-md-6 col-lg-4"><div class="card project" onClick="window.location.replace('{{ post.url }}')">
        <h4>{{ post.title }}</h4>
        <span class="role">{{ post.role }} </span><span class="company"> {{ post.company }} </span> <span class="location"> {{ post.location }} </span>

        <img src="{{ post.thumbnail }}" />
        <div class="excerpt">      {{ post.excerpt }}</div></div>
      </div>

    {% endfor %}
  </div>
  {%- endif -%}
{% endfor %}

