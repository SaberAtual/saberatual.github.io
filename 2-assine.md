---
layout: page
title: Cursos e assinaturas disponíveis
menu-title: Assine
permalink: /assine/
---

{% for curso in site.cursos %}

---

<article class="page-content">
    <div class="wrapper" data-grid="center spacing">
        <div data-cell="1of4 {% cycle 'order-1', '' %}">{% include svg{{ curso.url | remove: '.html' }}.svg %}</div>
        <div data-cell="3of4">
            <h3><a href="{{ site.baseurl }}{{ curso.url }}">{{ curso.title }}</a></h3>
            <p>{{ curso.excerpt }} <a href="{{ site.baseurl }}{{ curso.url }}">Leia mais...</a></p>
        </div>
    </div>
</article>

{% endfor %}
