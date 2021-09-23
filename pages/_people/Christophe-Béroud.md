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
  - IS_2021_Data
  - IS_2021_Exchange
---

## {{page.title}}

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; width: 80px; margin-top: -30px; margin-right: 10px;" src="{{ static_file.path | relative_url}}" />
  {%- endif -%}
{%- endfor -%}

Professor of Human Genetics  
Aix-Marseille University - INSERM  
Co-lead ELIXIR hCNV Community
ELIXIR-FR  

<!--more-->

* email [christophe.beroud@inserm.fr](mailto:christophe.beroud@inserm.fr)  
* web [MMG](https://www.marseille-medical-genetics.org/fr/c-beroud/)  
