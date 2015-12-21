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

<br>

<!-- Begin MailChimp Signup Form -->
<div id="mc_embed_signup">
<form action="//kylegraycar.us12.list-manage.com/subscribe/post?u=e90ebf818f100e659e91fd302&amp;id=48a1711bb6" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
  
<div class="mc-field-group">
  <label for="mce-EMAIL">Join my email list to keep up on new posts!</label>
  <div><input type="email" value="Enter email here" name="EMAIL" class="required email" id="mce-EMAIL"><input type="submit" value="Submit" name="subscribe" id="mc-embedded-subscribe" class="button">
    </div></div>
</div>
  <div id="mce-responses" class="clear">
    <div class="response" id="mce-error-response" style="display:none"></div>
    <div class="response" id="mce-success-response" style="display:none"></div>
  </div>
    <div style="position: absolute; left: -5000px;"><input type="text" name="b_e90ebf818f100e659e91fd302_48a1711bb6" tabindex="-1" value=""></div>
   
</form>
<p class="rss-subscribe" align="center">Or follow via <a href="{{ "/feed.xml" | prepend: site.baseurl }}">RSS</a></p>
</div>

<!--End mc_embed_signup-->

<div class="top-of-page"><a href="#top" class="toplink">^</a></div>

