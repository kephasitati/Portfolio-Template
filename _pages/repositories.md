---
layout: page
permalink: /coding-projects/
title: coding projects
description: I'm thrilled about these recent projects:
nav: true
nav_order: 2
---

**Health Prediction** [Code](https://github.com/galonpy/healthcare_example_notebook) Predicting healthcare status from prescription drug history! This causal inference model can predict a text health status of a new patient. This task was requested and reviewed by an insurance provider while I was at the University of Michigan.

**youtube_llm** [Code](https://github.com/galonpy/youtube_llm) | [Article](https://medium.com/@gabrielalon257/youtube-filtering-capstone-67f755fb6dca) | [Video](https://drive.google.com/file/d/10EIKd1QhmoLsq2TeQgsYkP51RMODiRMc/view)
Created a recommendation engine for browsing YouTube videos with LLMs. Made a PyTorch fine-tuned BERT, and leveraged the ChatGPT-API. Built using HuggingFace, AWS RDS, ETL, YouTube’s API, Docker, Json Data. Led a team of 4. Plays videos on a Streamlit website.

  
**mads-696-milestone-II-YouChoose** [Article](https://medium.com/@gabrielalon257/predicting-youtube-dislikes-4c71a41718ac)
This precedes the youtube_llm project above. This project explores unsupervised and supervised machine learning models to understand disliked videos on YouTube.


**This Website** I built this website in roughly three days without prior knowledge of front-end, HTML, Javascript, or CSS. I adapted it from [al-folio](https://github.com/alshedivat/al-folio) starter code that relies on Jekyll, and GitHub Actions for CI/CD.  


{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
  {% if site.data.repositories.github_users.size > 1 %}
  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.html username=user %}
  </div>

  ---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Repositories

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
