---
layout: page
permalink: /repositories/
title: repositories
description: These projects are eloquently explained with accompanied writing ':'
  **youtube_llm** [Medium Article](https://medium.com/@gabrielalon257/youtube-filtering-capstone-67f755fb6dca)
  **GR-GRIM** [Arxiv Publication] (https://arxiv.org/abs/2206.14348)
  **mads-696-milestone-II-YouChoose** [Medium Article](https://medium.com/@gabrielalon257/predicting-youtube-dislikes-4c71a41718ac)

#description: Edit the `_data/repositories.yml` and change the 3`github_users` and `github_repos` lists to include your own GitHub profile #and repositories.
nav: true
nav_order: 4
---

## GitHub users

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
