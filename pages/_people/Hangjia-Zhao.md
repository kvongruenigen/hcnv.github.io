---
title: "Hangjia Zhao"
layout: default
excerpt_link: https://info.baudisgroup.org/group/Hangjia_Zhao/
excerpt_separator: <!--more-->
category:
  - people
tags:
  - people
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

* Department of Molecular Life Sciences, University of Zurich
* [Progenetix](http://progenetix.org) project

<!--more-->
