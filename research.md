---
title: 研究ノート
permalink: /research/
section: research
description: 学んだこと、問い、考察を残す研究ノート。
---
学び

{% assign notes = site.research | sort: 'date' | reverse %}
<ul class="entries">
{% for note in notes %}
<li><time datetime="{{ note.date | date_to_xmlschema }}">{{ note.date | date: '%Y.%m.%d' }}</time><h3><a href="{{ note.url | relative_url }}">{{ note.title | escape }}</a></h3><p>{{ note.description | escape }}</p></li>
{% else %}<li>研究ノートは準備中です。</li>{% endfor %}
</ul>
