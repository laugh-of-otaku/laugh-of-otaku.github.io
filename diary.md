---
title: 日記
permalink: /diary/
section: diary
description: 日々の出来事と考えたことを、月ごとにまとめた日記。
---
日常

<ul class="entries">
{% for post in site.posts %}
<li><h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3><p>{{ post.description | escape }}</p></li>
{% else %}<li>日記は準備中です。</li>{% endfor %}
</ul>
