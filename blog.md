---
layout: page
title: Blog
tagline: Notes from the field
permalink: /blog.html
---

# The Blog, *coming soon*

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/Qx6tBsroYp4?rel=0&amp;controls=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
</iframe>
</center>

<div>
  <h2>Latest Posts</h2>
  <div>&nbsp;</div>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>

        {% assign date_format = site.cayman-blog.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}" title="{{ post.title }}">{{ post.title | escape }}</a>
        </h2>

        <span>{{ post.excerpt | markdownify | truncatewords: 30 }}</span>

      </li>
    {% endfor %}
  </ul>

</div>
