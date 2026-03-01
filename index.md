---
layout: default
title: Home
---

<div>
  <h2 style="border-bottom: 2px solid #E50914; padding-bottom: 10px; margin-bottom: 25px;">Latest Tales</h2>
  
  <div class="post-list">
    {% for post in site.posts %}
      <article style="background: transparent; border-bottom: 1px solid #ddd; padding-bottom: 20px; margin-bottom: 25px;">
        
        {% if post.image %}
          <a href="{{ post.url | relative_url }}" style="display: block; margin-bottom: 15px;">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="width: 100%; height: 250px; object-fit: cover; border-radius: 8px;">
          </a>
        {% endif %}

        <h3 style="margin-top: 0; margin-bottom: 8px;">
          <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #111; font-size: 20px; font-weight: bold; line-height: 1.4;">{{ post.title }}</a>
        </h3>
        
        <p style="font-size: 13px; color: #888; margin-top: 0; margin-bottom: 10px;">{{ post.date | date: "%d %B, %Y" }}</p>
        <p style="color: #555; font-size: 15px; line-height: 1.6;">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        
        <a href="{{ post.url | relative_url }}" style="display: inline-block; margin-top: 5px; font-weight: 600; color: #E50914; text-decoration: none;">Read More &raquo;</a>
      </article>
    {% endfor %}
  </div>
</div>
