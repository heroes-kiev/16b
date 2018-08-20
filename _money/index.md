---
layout: default
title: Отчеты и фонды
exclude: true
published: true
---

<ul class="list-unstyled">
{% for doc in site.money | sort: "date" | reverse %}
  {% if doc.exclude != true %}

    <li class="mt-3">
      <h5 class="mt-0 mb-1"><a href="{{doc.url}}">{{doc.sign_date}}: {{doc.title}}</a></h5>
    </li>

  {% endif %}
{% endfor %}
</ul>
