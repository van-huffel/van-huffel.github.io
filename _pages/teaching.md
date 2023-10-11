---
layout: page
permalink: /teaching/
title: teaching
titlecapital: Teaching
description: Course materials from my tenure as a teaching assistant during my Bachelor's and Master's studies at ETH Zurich.
nav: true
nav_order: 5
---

<div class="projects">
  <!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project vertically -->
  {%- for project in sorted_projects -%}
    <div class="grid"> 
    {% include projects.html %}
    </div>
  {%- endfor %}
</div>
