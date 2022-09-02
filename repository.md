---
layout: page
title: Repositories
description: The list of the repositories
lang: en
---
{% assign gh_page_repos = site.data.gh_pages %}
| Repository | GitHub Page (Document) |
|:-----------|:------------|
{%- for repository in site.github.public_repositories -%}
  {%- if repository.name == "ToshioCP.github.io" %}
    | [{{ repository.name }}]({{ repository.html_url }}) | <{{site.github.url}}> |
  {%- elsif gh_page_repos contains repository.name %}
    | [{{ repository.name }}]({{ repository.html_url }}) | <{{site.github.url}}/{{repository.name}}/> |
  {%- else %}
    | [{{ repository.name }}]({{ repository.html_url }}) | |
  {%- endif -%}
{%- endfor -%}