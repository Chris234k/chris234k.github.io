---
layout: default
---

{% for post in site.posts %}
  {% assign loopindex = forloop.index | modulo: 2 %}
  {% if loopindex == 1 %}
    <div>
      <a href="{{ post.url }}">{{ post.title }}</a>
  {% else %}
      <a href="{{ post.url }}">{{ post.title }}</a>
    </div>
  {% endif %}
{% endfor %}
