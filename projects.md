---
layout: post
title: Projects
---
<style>
.post-tile {
  display: flex;
  align-items: center;
  margin: 10px 0;
}
.post-thumbnail {
  width: 150px;
  height: 150px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  margin-right: 20px;
}
.post-details {
  flex: 1;
}
</style>


# Project

{% for post in site.posts %}
  {% for tag in post.tags %}
    {% if tag == "project" %}
<div class="post-tile">
  <a href="{{ site.baseurl }}{{ post.url }}">
    <div class="post-thumbnail" style="background-image: url('{{ site.baseurl }}{{ post.thumbnail }}');"></div>
  </a>
  <div class="post-details">
    <p><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></p>
    <p>{{ post.date | date_to_string }}</p>
  </div>
</div>
    {% break %}
    {% endif %}
  {% endfor %}
{% endfor %}