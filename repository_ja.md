---
layout: page
title: レポジトリ
description: The list of the repositories
lang: ja
---
{% assign gh_page_repos = site.data.gh_pages %}
| レポジトリ | GitHub Page (ドキュメント) |
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