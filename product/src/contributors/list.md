---
title : Contributors
subtitle : show them some love
layout : 'contrib.njk'
---
please take the time to support our contributors on other channels and read some of their other works.
If you would like to publish with us then please send us an email with a writing sample.
{%for post in collections.contrib%}

     {% include 'con-card-sm.njk' %}

{%endfor%}