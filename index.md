---
layout: base
---

<div class="home-page">
  <section class="hero">
    <h1>Financial Insights for Tomorrow's Markets</h1>
    <p>Expert analysis and market intelligence</p>
  </section>

  <section class="featured-posts">
    {% for post in site.posts %}
      <article class="post-card">
          <img class="post-image" src="{{ post.cover_image | default: '/assets/images/default-cover.png' }}" alt="{{ post.title }}">
        <div class="post-content">
          <div class="post-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %d, %Y" }}</time>
            <div class="post-tags">
              {% for tag in post.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          </div>
          <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
          <p class="subtitle">{{ post.subtitle }}</p>
        </div>
      </article>
    {% endfor %}
  </section>

</div>