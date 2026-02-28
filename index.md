---
layout: default
title: Home
---

<div>
  <h2 style="border-bottom: 2px solid #E50914; padding-bottom: 10px; margin-bottom: 25px;">Latest Tales</h2>
  
  <div class="post-list">
    {% for post in site.posts %}
      <article style="background: #fff; border: 1px solid #eee; border-radius: 8px; padding: 20px; margin-bottom: 20px; box-shadow: 0 2px 5px rgba(0,0,0,0.02);">
        <h3 style="margin-top: 0; margin-bottom: 8px;">
          <a href="{{ post.url }}" style="text-decoration: none; color: #111; font-size: 22px;">{{ post.title }}</a>
        </h3>
        <p style="font-size: 13px; color: #888; margin-top: 0; margin-bottom: 15px;">Published on: {{ post.date | date: "%B %d, %Y" }}</p>
        <p style="color: #555; font-size: 15px;">{{ post.excerpt | strip_html | truncatewords: 35 }}</p>
        <a href="{{ post.url }}" style="display: inline-block; margin-top: 10px; font-weight: 600; color: #E50914; text-decoration: none;">Read More &raquo;</a>
      </article>
    {% endfor %}
  </div>
</div>
