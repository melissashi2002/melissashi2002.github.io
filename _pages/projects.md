---
layout: page
title: Projects
permalink: /projects/
#description: A growing collection of your cool projects.
nav: true
nav_order: 3
display_categories: [research, course]
horizontal: false
---

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


## Research Projects

### Stock Predict Website
- **Duration**: Jan 2024 - May 2024
- **Description**:
  - Collaborated with a team to develop a full-stack web application for stock prediction using Python and Flask for the back-end.
  - Led front-end development with HTML and CSS, significantly improving user engagement.
  - Integrated machine learning models with scikit-learn and PyTorch for real-time updates and personalized user plans.



### GPAMAXXING
- **Duration**: June 2024 - Aug 2024
- **Description**:
  - Contributed to full-stack development of the GPAMAXXING website for GPA analysis and scheduling.
  - Designed user-friendly interfaces to enhance usability for academic planning.

![GPAMAXXING](path/to/image/gpamaxxing.jpg)

---

## Course Projects

### Cool Side Project
- **Duration**: March 2024
- **Description**:
  - Built an interactive web app for learning new programming languages.
  - Designed intuitive user interfaces and enhanced the user experience through responsive design.



### Chatbot Experiment
- **Duration**: June 2024 - Present
- **Description**:
  - Developed a chatbot using OpenAI's API to provide personalized responses for mental health self-management.
  - Conducted qualitative analysis on user interactions to improve chatbot capabilities.



<img src="/assets/img/Zenny.jpg" alt="Chatbot Experiment" style="width:70%; height:auto;">

---

## Academic Projects

### Research Paper on HCI and Mental Health
- **Duration**: Sept 2024 - Dec 2024
- **Description**:
  - Researched and wrote a paper on how human-computer interaction (HCI) can support mental health initiatives.
  - Presented findings at the annual tech conference at UIUC.


