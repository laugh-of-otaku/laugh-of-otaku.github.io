---
title: 日記
permalink: /diary/
section: diary
description: 日々の出来事と考えたことの記録。
---
日々の出来事と、考えたこと。

<ul class="entries">
{% for post in site.posts %}
<li><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%Y.%m.%d' }}</time><h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3><p>{{ post.description | escape }}</p></li>
{% else %}<li>日記は準備中です。</li>{% endfor %}
</ul>
