---
layout: page-fullwidth
title: Eagle Archive
#subheadline: "TODO"
description: "Past issues of The Eagle, the quarterly Carrollton Manor newsletter"
header:
   image: "various/sign1-crop-alternate-680x80.jpg"
   background-color:  "#fafafa"
permalink: "/resources/eagle-archive/"
breadcrumb: true
---

{% assign years = "2017|2016|2015|2014|2013|2012|2011|2010|2009|2008|2007|2006|2005|2004|2003|2002|2001" | split: "|" %}
{% assign thisYear = "2018" %}

{{ thisYear }}:  <a href="/resources/eagle-archive/eagle-{{ thisYear }}-spring.pdf">Spring</a> / <a href="/resources/eagle-archive/eagle-{{ thisYear }}-summer.pdf">Summer</a> / <a href="/resources/eagle-archive/eagle-{{ thisYear }}-fall.pdf">Fall</a> / <a href="/resources/eagle-archive/eagle-{{ thisYear }}-winter.pdf">Winter</a>
{% for yr in years %}
{{ yr }}:  <a href="/resources/eagle-archive/eagle-{{ yr }}-spring.pdf">Spring</a> / <a href="/resources/eagle-archive/eagle-{{ yr }}-summer.pdf">Summer</a> / <a href="/resources/eagle-archive/eagle-{{ yr }}-fall.pdf">Fall</a> / <a href="/resources/eagle-archive/eagle-{{ yr }}-winter.pdf">Winter</a>
{% endfor %}
