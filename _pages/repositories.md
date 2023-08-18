---
layout: page
permalink: /coding-projects/
title: coding projects
description: I led the direction of these large Python projects. They each took several months and were academically reviewed.
nav: true
nav_order: 2
---

**youtube_llm** [Article](https://medium.com/@gabrielalon257/youtube-filtering-capstone-67f755fb6dca) | [Video](https://drive.google.com/file/d/10EIKd1QhmoLsq2TeQgsYkP51RMODiRMc/view) | [Website](https://youtube-capstone.streamlit.app/)
This is a YouTube recommendation website that plays real videos and makes recommendations
using LLMs like BERT and ChatGPT to increase personalization.

**GR-GRIM** [Arxiv Publication](https://arxiv.org/abs/2206.14348)
Transformer neural networks are usually evaluated based on their top prediction per test question. We evaluate the broader
spectrum of outputs from the softmax function from where the top prediction are sourced from during training and testing. 
  
**mads-696-milestone-II-YouChoose** [Article](https://medium.com/@gabrielalon257/predicting-youtube-dislikes-4c71a41718ac)
This precedes the youtube_llm project above. This project explores unsupervised and supervised machine learning models to understand disliked videos on YouTube.

***

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
