---
layout: 'blog.njk'
---
{%for post in collections.misc%}

     {% include 'card.njk' %}

{%endfor%}