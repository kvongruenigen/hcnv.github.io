---
title: "Krzysztof Poterlowicz"
layout: default
excerpt_link:
excerpt_separator: <!--more-->
category:
  - people
tags:
  - people
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

* Elixir-UK Training Co-ordinator  
* Senior Lecturer in Bioinformatics and Biostatistics  
* University of Bradford, UK  

<!--more-->

* email [k.poterlowicz1@bradford.ac.uk](mailto:k.poterlowicz1@bradford.ac.uk)  
* web [BNradford U](https://www.bradford.ac.uk/staff/KPoterlowicz1)  
