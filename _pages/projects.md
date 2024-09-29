---
layout: page
title: projects
permalink: /projects/
description: A growing collection of my cool projects.
nav: true
nav_order: 3
display_categories: [development, web]
horizontal: false
---


<!-- pages/projects.md -->
<!-- pages/projects.md -->
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {% for category in page.display_categories %}
    <a id="{{ category }}" href=".#{{ category }}">
      <h2 class="category">{{ category }}</h2>
    </a>
    {% assign categorized_projects = site.projects | where: "category", category %}
    {% assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
      </div>
    </div>
    {% else %}
    <div class="row row-cols-1 row-cols-md-3">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
    {% endif %}
    {% endfor %}
  {% else %}
  <!-- Display projects without categories -->
  {% assign sorted_projects = site.projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
      </div>
    </div>
    {% else %}
    <div class="row row-cols-1 row-cols-md-3">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
    {% endif %}
  {% endif %}
</div>

<h2>Project Experience</h2>

<!-- Stock Predict Website -->
<h3>Stock Predict Website</h3>
<p><strong>Duration:</strong> Jan 2024 - May 2024</p>
<ul>
  <li>Collaborated with a team to develop a full-stack web application for stock prediction, using Python and Flask for the back-end architecture.</li>
  <li>Led the front-end development, creating intuitive and visually appealing user interfaces with HTML and CSS, which significantly improved user engagement and accessibility.</li>
  <li>Developed and integrated sophisticated machine learning models using scikit-learn and PyTorch, leveraging PyTrend and YFinance data within SQL databases to enable real-time updates and personalized user plans, while ensuring effective collaboration and project management to deliver a high-quality product.</li>
</ul>

<!-- GPAMAXXING -->
<h3>GPAMAXXING</h3>
<p><strong>Duration:</strong> June 2024 - Aug 2024</p>
<ul>
  <li>Full-Stack Development: Contributed to the development of the GPAMAXXING website, applying full-stack development skills to create a comprehensive platform for GPA analysis and class scheduling.</li>
  <li>Database System Integration: Implemented and managed database systems to efficiently handle student data and GPA calculations, ensuring accurate and reliable performance.</li>
  <li>User Interface Design: Designed and integrated user-friendly interfaces to facilitate students’ interaction with the GPA analysis tool, enhancing usability and accessibility for effective academic planning.</li>
</ul>
