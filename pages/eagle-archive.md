---
layout: page-fullwidth
title: Eagle Archive
#subheadline: "TODO"
description: "Past issues of The Eagle, the quarterly Carrollton Manor newsletter"
header:
   image: "header_image_alt.jpg"
   background-color:  "#fafafa"
permalink: "/resources/eagle-archive/"
breadcrumb: true
---
{% assign years = "2019|2018|2017|2016|2015|2014|2013|2012|2011|2010|2009|2008|2007|2006|2005|2004|2003|2002|2001" | split: "|" %}
{% assign thisYear = "2020" %}
{% assign thisSeason = "spring" %}

The Eagle is Carrollton Manor's quarterly newsletter.

Click <a href="/resources/eagle-archive/eagle-{{ thisYear }}-{{ thisSeason }}.pdf">here</a> for the current issue.

Search the entire archive:

{% include google_search_eagle_archive.html %}

<form style="padding-bottom: 0px;" onsubmit="google_search()" >
  <input type="text" id="google-search" placeholder="{{ site.data.language.enter_search_term }}">
</form>
Archive of past issues:

<!-- {{ thisYear }}:  <a href="/resources/eagle-archive/eagle-{{ thisYear }}-spring.pdf">Spring</a> -->
{% for yr in years %}
{{ yr }}:  <a href="/resources/eagle-archive/eagle-{{ yr }}-spring.pdf">Spring</a> / <a href="/resources/eagle-archive/eagle-{{ yr }}-summer.pdf">Summer</a> / <a href="/resources/eagle-archive/eagle-{{ yr }}-fall.pdf">Fall</a> / <a href="/resources/eagle-archive/eagle-{{ yr }}-winter.pdf">Winter</a>
{% endfor %}
