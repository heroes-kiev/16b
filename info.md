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
      docs size: {{collection.docs.size}}<br>
      docs size check: {% if collection.docs.size > 0 %} has docs {% else %} empty docs {% endif %}<br>
      big unless result: {{collection.label.eql? "posts" || collection.exclude == true || collection.output == false || collection.docs.size == 0}}<br>
      big unless results:<br>
      - posts: {{collection["label"].eql? "posts"}}<br>
      - exclude: {{collection.exclude == true}}<br>
      - output: {{collection.output == false}}<br>
      - size: {{collection.docs.size == 0}}<br>
      big unless: {% unless (collection.label.eql? "posts") || collection.exclude == true || collection.output == false || collection.docs.size == 0 %} can show {% else %} hide {% endunless %}<br>
      collection inspect:<br>
      <pre>{{collection | inspect}}</pre><br>
    </li>
  {% endfor %}
</ol>

#### categories:
<pre>{{ site.categories | inspect }}</pre>

#### collections content:
<pre>{{site.collections | inspect}}</pre>