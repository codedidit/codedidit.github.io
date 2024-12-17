---
title: "Blog"
layout: single
permalink: /blog/
classes:
  - wide
  - dark-theme
author_profile: true
---

<div class="blog-intro">
  Thoughts, tutorials, and insights about software development, cloud architecture, and emerging technologies.
</div>

```typescript
const blogTopics = {
  main: [
    'Software Architecture',
    'Web Development',
    'Cloud Solutions',
    'DevOps Practices'
  ],
  technologies: [
    'React/Vue',
    'Node.js',
    'AWS/Cloud',
    'CI/CD'
  ]
};
```

## Latest Posts

<div class="posts-grid">
{% for post in site.posts limit:3 %}
  <div class="post-card">
    {% if post.header.teaser %}
      <div class="post-card__image">
        <img src="{{ post.header.teaser }}" alt="{{ post.title }}">
      </div>
    {% endif %}
    <div class="post-card__content">
      <p class="post-card__meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%B %-d, %Y" }}
        </time>
        {% if post.category %}
          <span class="post-card__category">{{ post.category }}</span>
        {% endif %}
      </p>
      <h2 class="post-card__title">
        <a href="{{ post.url | relative_url }}" class="post-card__link">
          {{ post.title }}
        </a>
      </h2>
      <p class="post-card__excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
      <a href="{{ post.url | relative_url }}" class="btn btn--primary">Read More</a>
    </div>
  </div>
{% endfor %}
</div>

## Categories

<div class="categories-grid">
{% for category in site.categories %}
  <div class="category-card">
    <h3>{{ category[0] }}</h3>
    <ul>
      {% for post in category[1] limit:3 %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
</div>

## Newsletter
<div class="newsletter-signup">
  <h3>Stay Updated</h3>
  <p>Get notified about new posts and tutorials</p>
  <form class="newsletter-form" action="/subscribe" method="post">
    <input type="email" name="email" placeholder="Enter your email" required>
    <button type="submit" class="btn btn--primary">Subscribe</button>
  </form>
</div>
