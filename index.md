---
layout: page
title: Accueil
status: En cours
---

## Introduction

Plus de détails sur ce projet test [dans le README]({{site.baseurl}}/README.md)

## Quelques ressources utiles

- [Le guide de Don Rico](https://sites.google.com/site/donricoframasoft/)
- Etc.

## Avancement

<table class="table table-bordered">
{% assign sorted_pages = site.pages | sort:"name" %}
{% for item in sorted_pages  %}
{% if item.status %}
<tr>
    <td><a href="{{site.baseurl}}{{item.url}}">{{ item.title }}</a></td>
    <td><span class="label label-{% case item.status %}{% when 'Publié' or 'Publie' %}success{% when 'Relecture' %}warning{% when 'En cours' %}info{% else %}important{% endcase %}">{{ item.status }}</span></td>
</tr>
{% endif %}
{% endfor %}
</table>




