---
layout: home
title: "AI Talks"
---

<style>
  .centered {
    text-align: center;
    font-family: "Segoe UI", Roboto, sans-serif;
    padding: 2rem 1rem;
    max-width: 800px;
    margin: 0 auto;
  }

  .tagline {
    font-size: 1.2rem;
    color: #aaa;
    margin-top: -0.5rem;
    margin-bottom: 2rem;
    line-height: 1.6;
  }

  .cta-button {
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    border-radius: 8px;
    cursor: pointer;
    margin: 0.5rem;
    text-decoration: none;
    display: inline-block;
    transition: background 0.3s ease, color 0.3s ease, border 0.3s ease;
  }

  .primary {
    background-color: #00bcd4;
    color: #fff;
    border: none;
  }

  .primary:hover {
    background-color: #0097a7;
  }

  .secondary {
    border: 1px solid #00bcd4;
    background-color: transparent;
    color: #00bcd4;
  }

  .secondary:hover {
    background-color: #00bcd4;
    color: #fff;
  }

  .section-divider {
    margin: 3rem 0;
    border: none;
    border-top: 1px solid #333;
  }

  .section-heading {
    color: #00bcd4;
    font-size: 1.75rem;
    margin-bottom: 2rem;
  }

  .post-preview {
    margin-bottom: 2rem;
    text-align: left;
  }

  .post-preview a {
    color: #00bcd4;
    font-weight: 600;
    font-size: 1.25rem;
    text-decoration: none;
  }

  .post-preview a:hover {
    text-decoration: underline;
  }

  .post-date {
    color: #888;
    font-size: 0.9rem;
  }

  .archive-link {
    color: #00bcd4;
    font-weight: 500;
    text-decoration: none;
  }

  .archive-link:hover {
    text-decoration: underline;
  }
</style>

<div class="centered">
  <h1>🤖 AI Talks</h1>
  <p class="tagline">
    Welcome to my digital think tank where I explore the quirks, logic, beauty, and future of Artificial Intelligence.
  </p>

  <a href="{{ '/about/' | relative_url }}" class="cta-button primary">About Me</a>
  <a href="{{ '/' | relative_url }}" class="cta-button secondary">Read All Posts</a>
</div>

<hr class="section-divider" />

<div class="centered">
  <h2 class="section-heading">🔥 Recent Posts</h2>

  {% for post in site.posts limit:3 %}
    <div class="post-preview">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br />
      <small class="post-date">{{ post.date | date: "%B %d, %Y" }}</small><br />
      <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
    </div>
  {% endfor %}

  <p>
    <a href="{{ '/' | relative_url }}" class="archive-link">→ Browse the full archive</a>
  </p>
</div>
