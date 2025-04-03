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
      <div class="col-12 col-md-6 col-lg-4"><div class="card h-100 project" onClick="navigateTo('{{ post.url }}')">
            <div class="card-body">
                        <h5 class="card-title">{{ post.title }}</h5>
                        <p class="card-text">{{ post.excerpt }}</p>
                         </div>
                       <ul class="list-group list-group-flush">
                            <li class="list-group-item">{{ post.role }} </li>
                        </ul>
                        <img class="card-img-bottom" src="{{ post.thumbnail }}" />
                        <div class="card-footer">
                          <small class="text-body-secondary">{{ post.location }}</small> -
                          <small class="text-body-secondary">{{ post.company }}</small> 
                        </div>
            </div>
      </div>
    {% endfor %}
  </div>
  {%- endif -%}
{% endfor %}

