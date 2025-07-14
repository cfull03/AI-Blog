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
    margin: auto;
  }
  .tagline {
    font-size: 1.2rem;
    color: #ccc;
    margin-top: -10px;
    margin-bottom: 2rem;
  }
  .cta-button {
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    border-radius: 8px;
    cursor: pointer;
    margin: 0.5rem;
    text-decoration: none;
    display: inline-block;
  }
  .primary {
    background: #00bcd4;
    color: white;
    border: none;
  }
  .secondary {
    border: 1px solid #00bcd4;
    background: transparent;
    color: #00bcd4;
  }
  .section-divider {
    margin: 3rem 0;
    border: none;
    border-top: 1px solid #333;
  }
  .post-preview a {
    color: #00bcd4;
    font-weight: bold;
    font-size: 1.25rem;
    text-decoration: none;
  }
  .post-preview {
    margin-bottom: 1.5rem;
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
  <h2 style="color: #00bcd4;">🔥 Recent Posts</h2>

  {% for post in site.posts limit:3 %}
    <div class="post-preview">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br />
      <small style="color: #888;">{{ post.date | date: "%B %d, %Y" }}</small><br />
      <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
    </div>
  {% endfor %}

  <p>
    <a href="{{ '/' | relative_url }}" style="color: #00bcd4;">→ Browse the full archive</a>
  </p>
</div>
