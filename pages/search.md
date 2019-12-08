---
layout: page-fullwidth
title: Search
header:
   image: "header_image_alt.jpg"
   background-color:  "#fafafa"
permalink: "/search/"
show_meta: false
---

{% include google_search.html %}

<form style="padding-bottom: 200px;" onsubmit="google_search()" >
  <input type="text" id="google-search" placeholder="{{ site.data.language.enter_search_term }}">
</form>
