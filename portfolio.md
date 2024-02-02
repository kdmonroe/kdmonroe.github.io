---
layout: page
title: Portfolio
permalink: /portfolio/
---
projects:
  - name: "Project Name"
    description: "Project Description"
    image: "url-to-project-image"
    link: "url-to-project-page-or-github"
  - name: "Another Project"
    description: "Another Description"
    image: "url-to-another-project-image"
    link: "url-to-another-project-page-or-github"

{% for project in page.projects %}
  <div class="project">
    <h2>{{ project.name }}</h2>
    <p>{{ project.description }}</p>
    <!-- Add more project details here -->
  </div>
{% endfor %}
