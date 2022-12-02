---
layout: 'blog.njk'
---
{%for post in collections.series%}

     {% include 'card.njk' %}

{%endfor%}