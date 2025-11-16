---
layout: home
---

Udostępnione zapiski z tego, czego się ostatnio nauczyłem.

<article class="latest-post">
    {% assign latest_post = site.posts.first %}
    
    <header>
        <h2>Najnowszy Post: <a href="{{ latest_post.url | relative_url }}">{{ latest_post.title }}</a></h2>
        <p class="post-meta">{{ latest_post.date | date: "%Y-%m-%d" }}</p>
    </header>
    
    {{ latest_post.content }}
    
    <hr>
</article>

<div class="archive-list">
    <h3>Starsze posty:</h3>
    <ul>
    {% for post in site.posts offset: 1 %}
        <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span class="post-meta">— {{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
    {% endfor %}
    </ul>
</div>
