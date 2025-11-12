---
layout: default
title: "rambles"
permalink: /rambles/ # the permalink should match the page path
body_class: blog-page
---

<section id="blog-container">
  <div class="blog-grid">
    {% for post in site.posts %}
      <article class="blog-card">
        {% if post.featured_image %}
          <a href="{{ post.url | relative_url }}">
            <img src="{{ post.featured_image | relative_url }}" alt="{{ post.title }}">
          </a>
        {% endif %}
        <header>
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
        </header>
        <section class="excerpt">
          {{ post.excerpt }}
          <p><a href="{{ post.url | relative_url }}">Read more →</a></p>
        </section>
      </article>
    {% endfor %}
  </div>
</section>
