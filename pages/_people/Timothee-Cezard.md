---
title: "Timothee Cezard"
layout: default
excerpt_link:
excerpt_separator: <!--more-->
category:
  - contact
  - people
tags:
  - people
  - IS_2021_Exchange
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

* EMBL-EBI  
* Project Lead - The European Variation Archive  

<!--more-->

* email: tcezard [at] ebi.ac.uk
* web: [EBI](https://www.ebi.ac.uk/about/people/timothee-cezard)
* ORCID iD: [0000-0002-5626-270X](http://europepmc.org/search?query=AUTHORID:%220000-0002-5626-270X%22&sortby=Date)
