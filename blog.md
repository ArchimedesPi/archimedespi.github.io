---
layout: page
permalink: blog
---

# bloggyness
Sometimes I write things! Sometimes I put them here. They're probably not very good but writing is fun.

### posts
<ul>
{% for post in site.posts %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
{% endfor %}
</ul>

