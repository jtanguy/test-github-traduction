---
layout: page
title: Traduction
---

Introduction traduction blablabla

## Quelques ressources utiles

## Avancement

<table class="table">
{% tablerow item in site.posts cols: 2 %}
{% if tablerowloop.col_first %}
    {{ item.title }}
{% else %}
    {{ item.statut }}
{% endif %}
{% endtablerow %}
</table>




