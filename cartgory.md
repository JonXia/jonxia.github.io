---
layout: page
title: Cartgory
---
<div style="display:block;float:left;">
  {% for category in site.categories %}
  <h2>{{ category | first }}-{{ category | last | size }}篇</h2>
  <ul class="arc-list">
      {% for post in category.last %}
          <li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
  </ul>
  {% endfor %}
</div>