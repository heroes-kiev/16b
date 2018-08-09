---
layout: default
title: Документы
exclude: true
published: true
---

<ul class="list-unstyled">
{% for doc in site.docs %}

  <li class="media">
    <img class="mr-3" src="{{doc.img}}" alt="{{doc.title}}">
    <div class="media-body">
      <h5 class="mt-0 mb-1">{{doc.title}}</h5>
        {{doc.description}}
    </div>
  </li>
{% endfor %}
</ul>
