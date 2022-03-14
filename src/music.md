---
title: Music of the Synths
layout: page
page_class: " music"
---

{% assign albums = collections.albums.resources %}
{% for album in albums %}

  [![{{ album.title }}]({{ album.cover }})]({{ album.store_link }}){:target="yarred"}
  {:class="album-cover borderless-links"}

  {{ album.content }}

  [<i class="fa fa-play" aria-hidden="true"></i> Listen in Bandcamp]({{ album.store_link }}){:class="button large"}{:target="yarred"}
  {:class="cta-button small-text-center"}

  {% unless album.hide_streaming_links %}
  Stream in [Apple Music]({{ album.apple_music_link }}){:target="yarred"}
  {:class="small-text-center"}
  {% endunless %}

  <div style="clear:both"></div><br/>

{% endfor %}

## Older Projects
{:class="text-center"}

From 2007-2010, Yarred was part of an electronic music duo known as **Binary Sea**. They released two albums, [_Compass_](http://blazingedgeproductions.com/compass.html) (2008) and [_Land Ho!_](http://blazingedgeproductions.com/land_ho.html) (2010), featuring a wide array of ambient and electronica styles.

From 1993-2005, Yarred recorded and toured extensively with the Celtic & Early Music band **Distant Oaks**. Their magnum opus, [_Gach Là agus Oidhche: Music of Carmina Gadelica_](http://blazingedgeproductions.com/car_gad.html) (2003) is a tour de force of traditional yet surprisingly fresh Scottish Gaelic song and dance music. In the words of one Amazon reviewer, "if you are a fan of celtic music artfully done and with craft and heritage, this is a must-listen-to."