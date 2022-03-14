---
# Feel free to add content and custom Front Matter to this file.

layout: default
---

{% for post in collections.posts.resources %}
  <h2 class="post-title"><a href="{{ post.relative_url }}"><span>///</span> {{ post.title }} :: {{ post.date | date: "%-m.%-d.%Y" }} <span>///</span></a></h2>

  {{ post.content }}

  <div style="clear:both"></div><br/>
{% endfor %}
