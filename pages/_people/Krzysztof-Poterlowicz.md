---
title: "Krzysztof Poterlowicz"
layout: default
image_file: 'kpoterl.jpg'
excerpt_link:
excerpt_separator: <!--more-->
category:
  - contact
  - people
tags:
  - contacts
  - people
---

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; width: 80px; clear: none;" src="{{ static_file.path | relative_url}}" />
  {% endif %}
{% endfor %}

## {{page.title}}

Elixir-Uk Training Co-ordinator  
Senior Lecturer in Bioinformatics and Biostatistics
University of Bradfordy - UK  
ELIXIR-UK

<!--more-->

* email [k.poterlowicz1@bradford.ac.uk](mailto:k.poterlowicz1@bradford.ac.uk)  
* web [MMG]https://www.bradford.ac.uk/staff/KPoterlowicz1)  

