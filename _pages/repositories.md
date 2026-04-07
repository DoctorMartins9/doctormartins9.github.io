---
layout: page
permalink: /repositories/
title: repositories
description: Curated public repositories related to the research profile.
nav: false
nav_order: 4
---

This section is reserved for selected public code, tools, and reproducible research artifacts.

{% if site.data.repositories.github_users and site.data.repositories.github_users.size > 0 %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos and site.data.repositories.github_repos.size > 0 %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

{% unless site.data.repositories.github_users and site.data.repositories.github_users.size > 0 or site.data.repositories.github_repos and site.data.repositories.github_repos.size > 0 %}

No public repositories have been curated for display yet.

{% endunless %}
