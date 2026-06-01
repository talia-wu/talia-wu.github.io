---
layout: default
---
<section class="home-intro">
    <p>👋 Hi, this is <strong>Talia</strong>.</p>
    <p>I'm a product manager. This blog is where I document my thoughts and learning notes on <strong>vibe coding</strong> and <strong>product design</strong>.</p>
    <p>Feel free to reach out if you have any questions or ideas 😊</p>
</section>

<section class="posts-list">
    <h2>Latest Posts</h2>
    {% for post in site.posts limit:10 %}
    <article class="post-card">
        <a class="post-card-title" href="{{ post.url }}">{{ post.title }}</a>
        {% if post.excerpt %}
        <p class="post-card-excerpt">{{ post.excerpt | strip_html }}</p>
        {% endif %}
        <div class="post-card-meta">Date: {{ post.date | date: '%B %-d, %Y' }} | Author: {{ site.author }}</div>
    </article>
    {% endfor %}
    
    <p class="archive-link"><a href="/posts/">View all posts →</a></p>
</section>