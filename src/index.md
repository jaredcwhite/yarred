---
# Feel free to add content and custom Front Matter to this file.

layout: default
template_engine: serbea
---

<h1>Music News</h1>

{% posts = collections.posts.resources.reject { _1.data.tags.include?("TD2022") } %}
{% posts.each do |post| %}
  <h2 class="post-title"><a href="{{ post.relative_url }}"><span>///</span> {{ post.data.title }} :: {{ post.data.date.strftime("%-m.%-d.%Y") }} <span>///</span></a></h2>

  {{ post.content }}

  <div style="clear:both"></div><br/>
{% end %}

----

<h1>Latest in the “Best of Tangerine Dream” Series</h1>

{% tdposts = collections.posts.resources.select { _1.data.tags.include?("TD2022") }[0...2] %}
{% tdposts.each do |post| %}
  <h2 class="post-title"><a href="{{ post.relative_url }}"><span>///</span> {{ post.data.title | split: "<br/>" | last }} :: {{ post.data.date.strftime("%-m.%-d.%Y") }} <span>///</span></a></h2>

  {{ post.data.subtitle }}

  <div style="clear:both"></div><br/>
{% end %}

[More Posts This Way…](/tangerine-dream-2022/){:class="button large"}