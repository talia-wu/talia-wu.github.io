---
layout: default
---
<section class="home-intro">
    <h2>欢迎来到 Lia'Log</h2>
    <p>你好，我是 Lia（丹阳），一名产品经理。</p>
    <p>这个博客记录我在 vibe coding 和产品设计中的思考与学习笔记。</p>
    <p>希望这些内容对你也有帮助。如果有任何问题或想法，欢迎交流！</p>
</section>

<section class="posts-list">
    <h2>最新文章</h2>
    {% for post in site.posts limit:10 %}
    <div class="post-item">
        <span class="post-date">{{ post.date | date: '%Y-%m-%d' }}</span>
        <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt }}</p>
        {% endif %}
    </div>
    {% endfor %}
    
    <p class="archive-link"><a href="/posts/">查看全部文章 →</a></p>
</section>
