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
<tr>
    <td><a href="{{site.baseurl}}{{item.url}}">{{ item.title }}</a></td>
    <td><span class="label label-{% case item.status | downcase %}{% when publié or publie %}success{% when relecture %}warning{% else %}important{% endcase %}">{{ item.status }}</span></td>
</tr>
{% endif %}
{% endfor %}
</table>




