---
title: "Gary Saunders"
layout: default
image_file: "garys.jpg"
excerpt_separator: <!--more-->
category:
  - contact
  - people
tags:
  - contacts
  - people
---

<h2>{{page.title}}
{%- for static_file in site.static_files -%}
  {%- if static_file.path contains page.image_file -%}
<img style="float: right; width: 80px; margin-top: -12px; margin-right: 10px; margin-bottom: -50px;" src="{{ static_file.path | relative_url}}" />
  {%- endif -%}
{%- endfor -%}
</h2>

* ELIXIR h-CNV Coordinator  
* ELIXIR Hub  

<!--more-->

email [gary.saunders@elixir-europe.org](mailto:elixir-europe.org)
