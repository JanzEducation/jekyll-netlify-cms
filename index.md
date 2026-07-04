---
layout: default
title: Home
---

<!-- ================= HERO ================= -->

<section class="hero">

<div class="hero-left">

<span class="breaking">🔥 BREAKING</span>

<h1>Stories That Matter.<br>Truth That Lasts.</h1>

<p>
Welcome to <strong>JANZ TALES</strong>, your trusted source
for news, explainers, technology, education and inspiring stories.
</p>

<a href="#latest" class="hero-btn">
Explore Stories →
</a>

</div>

<div class="hero-right">

{% assign featured = site.posts.first %}

{% if featured.image %}

<a href="{{ featured.url | relative_url }}">

<img src="{{ featured.image | relative_url }}" alt="{{ featured.title }}">

</a>

{% endif %}

<div class="featured-card">

<span class="badge">FEATURED</span>

<h2>

<a href="{{ featured.url | relative_url }}">

{{ featured.title }}

</a>

</h2>

<p>

{{ featured.excerpt | strip_html | truncatewords:25 }}

</p>

</div>

</div>

</section>

<!-- ================= BREAKING NEWS ================= -->

<section class="ticker">

<div class="ticker-title">

LIVE

</div>

<div class="ticker-content">

<marquee scrollamount="5">

{% for post in site.posts limit:10 %}

📰

<a href="{{ post.url | relative_url }}">

{{ post.title }}

</a>

&nbsp;&nbsp;&nbsp;&nbsp;

{% endfor %}

</marquee>

</div>

</section>

<!-- ================= EDITOR PICKS ================= -->

<section class="editor-section">

<h2 class="section-title">

⭐ Editor's Picks

</h2>

<div class="editor-grid">

{% for post in site.posts limit:3 %}

<div class="editor-card">

{% if post.image %}

<a href="{{ post.url | relative_url }}">

<img src="{{ post.image | relative_url }}">

</a>

{% endif %}

<div class="editor-content">

<h3>

<a href="{{ post.url | relative_url }}">

{{ post.title }}

</a>

</h3>

<p>

{{ post.excerpt | strip_html | truncatewords:18 }}

</p>

<a href="{{ post.url | relative_url }}" class="read-btn">

Read More →

</a>

</div>

</div>

{% endfor %}

</div>

</section>

<!-- ================= LATEST ================= -->

<section id="latest">

<h2 class="section-title">

📰 Latest Tales

</h2>

<div class="post-grid">

{% for post in site.posts offset:3 %}

<div class="post-card">

{% if post.image %}

<a href="{{ post.url | relative_url }}">

<img src="{{ post.image | relative_url }}">

</a>

{% endif %}

<div class="post-content">

<span class="date">

📅 {{ post.date | date:"%d %b %Y" }}

</span>

<h3>

<a href="{{ post.url | relative_url }}">

{{ post.title }}

</a>

</h3>

<p>

{{ post.excerpt | strip_html | truncatewords:22 }}

</p>

<a href="{{ post.url | relative_url }}" class="read-btn">

Continue Reading →

</a>

</div>

</div>

{% endfor %}

</div>

</section>
