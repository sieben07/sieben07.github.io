---
layout: default
title: Mächtig viele Worte!
title2: Wenn man am Boden liegt,
title3: hat man Zeit die Sterne zu sehen.
---
{% for post in site.posts limit:5 %}
<section class="well">
    <span>
        {{ post.date | date_to_string }}
    </span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    {{ post.content | replace:'more start -->','' | replace:'<!-- more end','' }}
<a href="{{ post.url }}">Weiter lesen...</a>
</section>
{% endfor %}
