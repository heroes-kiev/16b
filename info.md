---
layout: default
title: Info
published: true
exclude: true
---

#### commit:
<pre>{{ site.github.build_revision }}</pre>

#### collection size:
<pre>{{site.collections[0].docs | size}}</pre>

#### collections content:
<pre>{{site.collections | inspect}}</pre>