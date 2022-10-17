---
title: The Best of Tangerine Dream
layout: page
template_engine: serbea
---

**A blog series with a new post every day to round out 2022!**
{:style="color:white;font-size:120%;text-align:center"}

----

{% tdposts = collections.posts.resources.select { _1.data.tags.include?("TD2022") } %}
{% tdposts.each do |post| %}
  <h2 class="post-title"><a href="{{ post.relative_url }}"><span>///</span> {{ post.data.title | split: "<br/>" | last }} :: {{ post.data.date.strftime("%-m.%-d.%Y") }} <span>///</span></a></h2>

  {{ post.data.subtitle }}

  <div style="clear:both"></div><br/>
{% end %}