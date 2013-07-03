---
layout: page
title: Accueil
---

Introduction traduction blablabla

## Quelques ressources utiles

- [Le guide de Don Rico](https://sites.google.com/site/donricoframasoft/)
- Etc.

## Avancement

<table class="table table-bordered">
{% assign sorted_pages = site.pages | sort:"name" %}
{% for item in sorted_pages  %}
{% if item.status %}
<tr><td><a href="{{site.baseurl}}{{item.url}}">{{ item.title }}</a></td><td>{{ item.status }}</td></tr>
{% endif %}
{% endfor %}
</table>




