---
layout: default
title: Документы
exclude: true
published: true
---

<ul class="list-unstyled">
{% for doc in site.docs | sort: "title" %}
  {% if doc.exclude != true %}

    <li class="media mt-5">
      <a href="{{doc.url}}" style="text-align: center; width: 170px"><img class="mr-3" style="max-height: 150px; max-width: 150px;" src="{{doc.picture}}" alt="{{doc.title}}"></a>
      <div class="media-body">
        <h5 class="mt-0 mb-1"><a href="{{doc.url}}">{{doc.title}}</a></h5>
          {{doc.description}}
      </div>
    </li>

  {% endif %}
{% endfor %}
</ul>
