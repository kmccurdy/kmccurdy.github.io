---
layout: page
permalink: /publications/
title: publications
description: 
years: [2020, 2019, 2017, 2013, 2010]
---

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f publications -q @*[year={{y}}]* %}
{% endfor %}
