---
layout: default
title: Home
---

<style>
.page-title{
font-size:34px;
font-weight:800;
margin:30px 0;
background:linear-gradient(90deg,#ff2d55,#ff0000);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.post-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(340px,1fr));
gap:28px;
}

.post-card{
background:#fff;
border-radius:18px;
overflow:hidden;
box-shadow:0 15px 40px rgba(0,0,0,.08);
transition:.4s;
animation:fadeUp .8s ease both;
}

.post-card:hover{
transform:translateY(-10px);
box-shadow:0 25px 60px rgba(229,9,20,.18);
}

.post-image{
height:240px;
overflow:hidden;
}

.post-image img{
width:100%;
height:100%;
object-fit:cover;
transition:.5s;
}

.post-card:hover img{
transform:scale(1.08);
}

.post-content{
padding:22px;
}

.post-title{
font-size:24px;
font-weight:800;
line-height:1.4;
margin-bottom:12px;
}

.post-title a{
color:#111;
text-decoration:none;
}

.post-title a:hover{
color:#E50914;
}

.post-date{
font-size:13px;
color:#999;
margin-bottom:14px;
}

.post-excerpt{
font-size:16px;
color:#555;
line-height:1.8;
margin-bottom:20px;
}

.read-btn{
display:inline-flex;
align-items:center;
gap:10px;
padding:12px 22px;
background:linear-gradient(90deg,#ff1f3d,#E50914);
color:#fff;
border-radius:40px;
text-decoration:none;
font-weight:700;
transition:.35s;
box-shadow:0 10px 25px rgba(229,9,20,.35);
}

.read-btn:hover{
transform:translateX(6px);
}

@keyframes fadeUp{
from{
opacity:0;
transform:translateY(30px);
}
to{
opacity:1;
transform:translateY(0);
}
}
</style>

<h1 class="page-title">
🔥 Latest Tales
</h1>

<div class="post-grid">

{% for post in site.posts %}

<div class="post-card">

{% if post.image %}
<div class="post-image">
<a href="{{ post.url | relative_url }}">
<img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
</a>
</div>
{% endif %}

<div class="post-content">

<div class="post-title">
<a href="{{ post.url | relative_url }}">
{{ post.title }}
</a>
</div>

<div class="post-date">
📅 {{ post.date | date: "%d %B, %Y" }}
</div>

<div class="post-excerpt">
{{ post.excerpt | strip_html | truncatewords: 24 }}
</div>

<a class="read-btn" href="{{ post.url | relative_url }}">
Read More →
</a>

</div>

</div>

{% endfor %}

</div>
