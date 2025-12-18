---
layout: page
title: Team
permalink: /team/
description: The Medical Computer Vision Lab Team
subtitle: <a href='https://www.uvic.ca/ecs/computerscience/index.php'>Engineering & Computer Science Building</a>. Room 562. 3800 Finnerty Road. 
nav: true
nav_order: 7

groups: [members, visitors]

members:
  title: Members
  people:
    - name: Ashery Mbilinyi
      description: Head 
      website: https://asherymbilinyi.github.io/
      picture: headshot.png

    - name: Nidita Roy
      description: MSc Student
      website: https://scholar.google.ca/citations?user=n67PhNEAAAAJ&hl=en&oi=ao
      picture: 

    - name: Amirhossein Roodaki
      description: MSc Student
      website: https://orcid.org/0009-0008-5765-0529
      picture: amirhossein.jpeg
      

    - name: Rishabh Jha
      description: MSc Student
      website: https://www.linkedin.com/in/rishabhjhatheaiguy/
      picture: rishabh.jpeg

visitors:
  title: Visitors/Interns
  people:
    - name: Smit Amin
      description: BSc Student
      website:
      picture: 

  
    - name: Cornelius Maroa
      description: Intern
      website: https://marwamasese.netlify.app/
      picture: cornelius.jpg
---



<div class="projects">
  {%- for group in page.groups -%}
    <h2 class="category">{{ page.[group].title }}</h2>
    <div class="grid">
      {%- for person in page.[group].people -%}
        <article class="grid-item card">
          {% if person.picture %}
            <img class="avatar" src="/assets/img/{{ person.picture }}" alt="{{ person.name }}">
          {% endif %}

          <div class="card-body">
            <h2 class="card-title">
              {% if person.website %}
                <a href="{{ person.website }}">{{ person.name }}</a>
              {% else %}
                {{ person.name }}
              {% endif %}
            </h2>

            <div class="card-text">
              {{ person.description }}
              {% if person.office %}
                <p>{{ person.office }}</p>
              {% endif %}
              {% if person.address %}
                <p>{{ person.address }}</p>
              {% endif %}
            </div>
          </div>
        </article>
      {%- endfor -%}
    </div>
  {%- endfor -%}
</div>
