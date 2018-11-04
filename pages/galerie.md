---
layout: page

namespace: galerie
permalink: galerie/
permalink_ru: galereya/

cover_image: palomniki.jpg
title: pages.gallery
---
{% jekyllgram 6 %}
   <a href="{{ photo.link }}" title="{{ photo.caption.text }}">
     <img src="{{ photo.images.thumbnail.url }}" title="{{ photo.caption.text }}" />
   </a>
{% endjekyllgram %}
