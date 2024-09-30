---
layout: cv
title: CV
permalink: /cv/
nav: true
nav_order: 5
cv_pdf: example_pdf.pdf
toc:
  sidebar: left
---

{% comment %}
This is the CV page. Modify content or pull data from cv.yml.
{% endcomment %}

## Download PDF
[Download my CV]({{ site.baseurl }}/assets/cv/example_pdf.pdf)

## Education
{% include cv/education.liquid %}

## Work Experience
{% include cv/work.liquid %}

## Projects
{% include cv/projects.liquid %}

## Skills
{% include cv/skills.liquid %}
