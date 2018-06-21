---
layout: page
mtitle: Phase 1
title: "Phase 1: SANTA"
subtitle: Systematic Analysis of Narrative Texts through Annotation
add_to_menu: true
index: 100
---


<ul class="posts">
  {% assign posts = site.posts | where:"phase","1" %}
  {% for post in posts %}
  {% include date.html date=post.date lang=post.lang%}
	{% include teaser.html post=post %}
  {% endfor %}
</ul>
