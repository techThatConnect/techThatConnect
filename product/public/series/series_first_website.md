---
title: First Website
subtitle: this website
layout: 'blog.njk'
tags: 'series'
url: '/series/series_first_website'
---
{%for post in collections.series_first_website%}

     {% include 'card.njk' %}

{%endfor%}