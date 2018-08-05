---
layout: default
title: Info
published: true
exclude: true
---

#### commit:
<pre>{{ site.github.build_revision }}</pre>

#### collection size:
<ol>
  {% for collection in site.collections %}
    <li> <b>collection</b><br>
      size: {{collection.docs.size}}<br>
      compare: {{collection.docs.size > 0}}<br>
      compare if: {% if collection.docs.size > 0 %} more {% else %} no more {% endif %}<br>
      collection inspect:<br>
      <pre>{{collection | inspect}}</pre><br>
      collection[1]:<br>
      <pre>{{collection[1] | inspect}}</pre>
    </li>
  {% endfor %}
</ol>

#### collections content:
<pre>{{site.collections | inspect}}</pre>