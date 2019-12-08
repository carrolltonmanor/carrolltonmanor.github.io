---
layout: page-fullwidth
subheadline:  "Gallery"
title:  "Planting Day and Yard Sale - 2014"
header:
   image: "various/sign1-crop-alternate-680x80.jpg"
   background-color:  "#fafafa"
categories:
    - gallery
tags:
    - 
show_meta: true
breadcrumb: true
---

{% assign TOTAL_PICS_NO = 12 %}
{% assign FOLDER_NAME = '2014-04-24-planting-day-and-yard-sale' %}
<ul class="clearing-thumbs small-block-grid-3" data-clearing>
{% for i in (1..TOTAL_PICS_NO) %}
  <li><a href="{{ site.url }}/images/{{ FOLDER_NAME }}/{{ i }}.jpg"><img  data-caption="" class="th" src="{{ site.url }}/images/{{ FOLDER_NAME }}/{{ i }}_thumb.jpg"></a></li>
{% endfor %}
</ul>