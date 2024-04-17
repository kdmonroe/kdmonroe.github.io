---
layout: page
title: Projects
permalink: /portfolio/
---


{% for post in site.categories['project'] %}
  <div class="project">
    <img src="{{ post.thumbnail }}" alt="{{ post.title }}" class="rounded">
    <div class="project-info">
      <!-- Make the title a link to the post -->
      <h3>
        <a href="{{ post.url | relative_url }}" class="project-title-link">{{ post.title }}</a>
      </h3>
      <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <div class="project-meta">
        {% if post.categories.size > 0 %}
          <!-- Use the category to create a specific class for each label -->
          <div class="post-categories">
            {% for category in post.categories %}
              <span class="category-label category-{{ category | slugify }}">{{ category }}</span>
            {% endfor %}
          </div>
        {% endif %}
        <!-- Check if there's a GitHub URL before displaying the link -->
        {% if post.github_url %}
          <a href="{{ post.github_url }}" class="github-link" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-github"></i>
          </a>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
