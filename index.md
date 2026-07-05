---
layout: default
title: Home
---

<div class="home-container">
  <header class="home-header">
    <h1 class="page-heading">Latest Updates from Janz Education</h1>
    <p>Welcome to our learning platform.</p>
  </header>

  <!-- Jekyll Loop to Fetch Posts -->
  {% if site.posts.size > 0 %}
    <ul class="post-list">
      {% for post in site.posts %}
        <li class="post-item">
          <!-- Post Date -->
          <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
          
          <!-- Post Title and Link -->
          <h2 class="post-title">
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </h2>
          
          <!-- Post Excerpt (Summary) -->
          <div class="post-excerpt">
            {{ post.excerpt }}
          </div>
          
          <a href="{{ post.url | relative_url }}" class="read-more">Read More &raquo;</a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p class="no-posts">No posts found. Start writing in your Netlify CMS!</p>
  {% endif %}
</div>

<!-- Basic CSS for the layout -->
<style>
  .home-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  }
  .home-header {
    text-align: center;
    margin-bottom: 40px;
  }
  .post-list {
    list-style: none;
    padding: 0;
  }
  .post-item {
    margin-bottom: 30px;
    padding-bottom: 20px;
    border-bottom: 1px solid #eee;
  }
  .post-meta {
    font-size: 0.85em;
    color: #666;
  }
  .post-title {
    margin: 5px 0 10px;
  }
  .post-link {
    text-decoration: none;
    color: #e50914; /* Janz Red */
  }
  .post-link:hover {
    text-decoration: underline;
  }
  .read-more {
    display: inline-block;
    margin-top: 10px;
    font-weight: bold;
    color: #333;
    text-decoration: none;
  }
</style>
