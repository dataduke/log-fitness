---
layout: page
title: About Swim, Bike, Run, Gym & Yoga
---
<div class="row-fluid post-full">
  <div class="span12">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
  <h3>{{ y }}</h3>
  {% endif %}
<ul class="articles-article">
  <li>
  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
  <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  {{ post.line }}
  </li>
</ul>
<br/>
{% endfor %}
  </div>
</div>