
<h2>Tags</h2>
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  
    {% for post in tag[1] %}

<a href="{{ post.url }}">{{ post.title }}</a>
    {% endfor %}
  
{% endfor %}

<h2>Categories</h2>
{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  
    {% for post in category[1] %}
  <a href="{{ post.url }}">{{ post.title }}</a>
    {% endfor %}
  
{% endfor %}