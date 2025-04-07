---
layout: default
title: Alle Einträge
title2: Hier sind alle,
title3: Einträge chronologisch sortiert!
---
<ul class="well">
{% for post in site.posts %}
    <li><a href="{{ post.url }}">/*{{ post.date | date:"%d.%m.%Y" }} {{ post.title }} */</a></li>
{% endfor %}
</ul>
