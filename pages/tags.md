---
layout: default
title: Tags
permalink: /tags/
---

<article class="container-page">
  <h1 class="page-title">{{ site.data.lang[site.language].tags_title }}</h1>
  <ul class="categories-list">
    {% for tag in site.tags %}
    <li id="{{ tag | first }}">{{ tag | first }}
    {% assign sorted_posts = site.posts | sort: 'date' %}{% for post in sorted_posts %}{%if post.tags contains tag[0]%}
      <div class="posts-list-item">
        <span class="posts-list-item-name float-left"><a href="{{ post.url }}">{{ post.title }}</a></span>
        <span class="posts-list-item-date float-right">{{ post.date | date: "%Y-%m-%d" }}</span>
      </div>
    {% endif %}{% endfor %}
    </li>
    {% endfor %}
  </ul>
</article>

