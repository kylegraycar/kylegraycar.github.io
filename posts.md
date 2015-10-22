---
layout: page
title: Blog 博客
permalink: /blog/
---

<ul class="post-list" align="center">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p>
          {{ post.description }}
        </p>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe" align="center"><a href="{{ "/feed.xml" | prepend: site.baseurl }}">RSS</a></p>