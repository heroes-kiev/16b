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
      compare if: {% if collection.docs.size > 0 %} more {% else %} no more {% endif %}<br>
      big if result: {{collection.label != "posts" && !collection.exclude && collection.output && collection.docs.size > 0}}<br>
      big if results:<br>
      - posts: {{collection.label != "posts"}}<br>
      - exclude: {{!collection.exclude}}<br>
      - output: {{collection.output}}<br>
      - size: {{collection.docs.size > 0}}<br>
      big if: {% if collection.label != "posts" && !collection.exclude && collection.output && collection.docs.size > 0 %} can show {% else %} hide {% endif %}<br>
      collection inspect:<br>
      <pre>{{collection | inspect}}</pre><br>
    </li>
  {% endfor %}
</ol>

#### categories:
<pre>{{ site.categories | inspect }}</pre>

#### collections content:
<pre>{{site.collections | inspect}}</pre>