---
title: "Christophe Béroud"
layout: default
image_file: 'cberoud.png'
excerpt_link:
excerpt_separator: <!--more-->
category:
  - contact
  - people
tags:
  - contacts
  - people
  - .featured
---

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; width: 80px;" src="{{ static_file.path | relative_url}}" />
  {% endif %}
{% endfor %}

## {{page.title}}

ELIXIR h-CNV project lead  
Aix-Marseille University - INSERM  
ELIXIR-FR  

<!--more-->

* email [christophe.beroud@inserm.fr](mailto:christophe.beroud@inserm.fr)  
* web [MMG](https://www.marseille-medical-genetics.org/fr/c-beroud/)  

