---
layout: page-fullwidth
title: Contact Us
#subheadline: "TODO"
description: "Contact Us"
header:
   image: "various/sign1-crop-alternate-680x80.jpg"
   background-color:  "#ffe6b3"
permalink: "/contact/"
breadcrumb: true
---

For more information about the Community or the <a href="/cmia">CMIA</a>, contact the following folks:

{% for person in site.data.board_roles %}

  {% assign this_phone = site.data.people | map: person.id | map: 'phone' %}
  {% assign this_email = site.data.people | map: person.id | map: 'email' %}

  {{ site.data.people | map: person.id | map: 'name'}} ({{ person.title }}):  {{ this_phone }} / {{ this_email }}
  
{% endfor %}


For suggestions on improving this site, <a href="mailto:carrolltonmanorweb@gmail.com">email us</a>.