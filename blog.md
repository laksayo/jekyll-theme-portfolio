---
layout: default
title: "rambles"
---

# rambles

<div class="blog-posts">
    {% for post in site.posts %}
        <article>
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <p>{{ post.excerpt }}</p>
        </article>
    {% endfor %}
</div>
