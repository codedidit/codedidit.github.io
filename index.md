---
layout: single
classes:
  - wide
  - dark-theme
author_profile: true
---

<div class="hero-intro">
  Hi, I'm Codedidit! 👋 Founder of Genius Circus, creator of Papert, and a lifelong learner passionate about integrating AI into business, education, and mental health initiatives.
</div>

## Current Ventures

```typescript
const innovations = {
  education: {
    name: 'Papert',
    type: 'AI-Driven Learning Platform',
    target: 'Grades 6-12',
    mission: 'Free personalized learning for all'
  },
  startup: {
    name: 'Foundair',
    type: 'AI-Powered Startup Builder',
    focus: 'Idea validation & solution building',
    tools: ['Problem discovery', 'Market research']
  },
  impact: {
    name: "Joan's Help",
    type: 'Mental Health Nonprofit',
    reach: '2000+ families served',
    mission: 'Free mental health resources'
  }
};
```

<div class="feature-grid">
  <div class="feature-card">
    <h3>🌟 Innovation</h3>
    <p>Creating AI-driven solutions for education, business, and mental health.</p>
  </div>
  
  <div class="feature-card">
    <h3>🧠 Expertise</h3>
    <p>Full-stack development, AI integration, and prompt engineering.</p>
  </div>
  
  <div class="feature-card">
    <h3>💡 Impact</h3>
    <p>Building tools and platforms that make a difference globally.</p>
  </div>
</div>

## Latest Projects
{% for post in site.posts limit:2 %}
  {% if post.categories contains "project" %}
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    {{ post.excerpt }}
  {% endif %}
{% endfor %}
