---
layout: page-fullwidth
title: Photo Gallery
#subheadline: "TODO"
description: "Photo Gallery"
header:
   image: "header_image_alt.jpg"
   background-color:  "#fafafa"
permalink: "/gallery/"
breadcrumb: true
---

<ul>
    {% for post in site.categories.gallery %}
    <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
