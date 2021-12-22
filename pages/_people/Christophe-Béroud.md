---
title: "Christophe Beroud"
layout: default
excerpt_link:
excerpt_separator: <!--more-->
category:
  - people
tags:
  - contacts
  - people
  - .featured
  - IS_2021_Data
  - IS_2021_hCNV-X
---

<h2>{{page.title}}
{%- assign portrait = page.title | replace: ' ', '-' -%}
{%- for static_file in site.static_files -%}
    {%- if static_file.extname == '.jpg' or static_file.extname == '.png'  -%}
        {%- assign imgf = static_file.basename | replace: ' ', '-' -%}
        {%- if imgf == portrait -%}
<img style="float: right; width: 80px; margin-top: -12px; margin-right: 10px; margin-bottom: -50px;" src="{{ static_file.path | relative_url}}" />
        {%- endif -%}
    {%- endif -%}
{%- endfor -%}</h2>

* Professor of Human Genetics  
* Aix-Marseille University - INSERM  
* Co-lead ELIXIR hCNV Community
* ELIXIR-FR  

<!--more-->

* email [christophe.beroud@inserm.fr](mailto:christophe.beroud@inserm.fr)  
* web [MMG](https://www.marseille-medical-genetics.org/fr/c-beroud/)  
