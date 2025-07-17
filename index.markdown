---
layout: home
title: "AI Talks"
---

<link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet">

<style>
  body {
    background-color: #0d1117;
    color: #c9d1d9;
    font-family: 'Fira Code', monospace;
  }

  a {
    color: #58a6ff;
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  .centered {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem 1rem;
    text-align: center;
  }

  .terminal {
    background: #161b22;
    border-radius: 8px;
    padding: 2rem;
    margin-bottom: 2rem;
    box-shadow: 0 0 0 1px #30363d;
    text-align: left;
    font-size: 0.95rem;
  }

  .terminal-header {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
  }

  .dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    margin-right: 6px;
  }

  .red { background: #ff5f56 }
  .yellow { background: #ffbd2e }
  .green { background: #27c93f }

  .title {
    margin-left: auto;
    font-size: 0.85rem;
    color: #8b949e;
  }

  .prompt {
    color: #00ff87;
  }

  .tagline {
    margin-top: 1rem;
    color: #8b949e;
    font-size: 1rem;
    line-height: 1.6;
  }

  .cta-button {
    padding: 0.75rem 1.5rem;
    font-size: 0.95rem;
    border-radius: 6px;
    margin: 0.5rem;
    display: inline-block;
    transition: all 0.25s ease;
  }

  .primary {
    background-color: #238636;
    color: #fff;
    border: none;
  }

  .primary:hover {
    background-color: #2ea043;
  }

  .secondary {
    border: 1px solid #58a6ff;
    background: transparent;
    color: #58a6ff;
  }

  .secondary:hover {
    background-color: #58a6ff;
    color: #0d1117;
  }

  .section-divider {
    margin: 3rem 0;
    border-top: 1px solid #30363d;
  }

  .section-heading {
    font-size: 1.5rem;
    color: #58a6ff;
    margin-bottom: 2rem;
  }

  .post-preview {
    text-align: left;
    margin-bottom: 2rem;
    background: #161b22;
    padding: 1.25rem;
    border-radius: 6px;
    border: 1px solid #30363d;
    transition: transform 0.2s ease;
  }

  .post-preview:hover {
    transform: translateY(-2px);
  }

  .post-date {
    font-size: 0.85rem;
    color: #8b949e;
  }

  .archive-link {
    display: inline-block;
    margin-top: 1rem;
    font-weight: 500;
    color: #58a6ff;
  }
</style>

<div class="centered">
  <div class="terminal">
    <div class="terminal-header">
      <span class="dot red"></span>
      <span class="dot yellow"></span>
      <span class="dot green"></span>
      <span class="title">~/ai-talks</span>
    </div>
    <div class="terminal-body">
      <p><span class="prompt">ai@localhost</span>:~$ Welcome to <strong>AI Talks</strong></p>
      <p class="tagline">A digital lab where I explore the quirks, logic, beauty, and future of artificial intelligence.</p>
    </div>
  </div>

  <a href="{{ '/about/' | relative_url }}" class="cta-button primary">About Me</a>
  <a href="{{ '/' | relative_url }}" class="cta-button secondary">Read All Posts</a>
</div>

<hr class="section-divider" />

<div class="centered">
  <h2 class="section-heading">🧠 Latest Thinking</h2>

  {% for post in site.posts limit:3 %}
    <div class="post-card">
      <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <p class="post-meta">{{ post.date | date: "%b %d, %Y" }}</p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
    </div>
  {% endfor %}

  <a href="{{ '/' | relative_url }}" class="archive-link">→ Browse all posts</a>
</div>

