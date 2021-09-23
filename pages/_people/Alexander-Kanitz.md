---
title: "Alexander Kanitz"
layout: default
image_file: 'akanitz.jpg'
excerpt_link:
excerpt_separator: <!--more-->
category:
  - contact
  - people
tags:
  - contacts
  - people
  - IS_2021_Exchange
---

<h2>{{page.title}}
{%- for static_file in site.static_files -%}
  {%- if static_file.path contains page.image_file -%}
<img style="float: right; width: 80px; margin-top: -12px; margin-right: 10px; margin-bottom: -50px;" src="{{ static_file.path | relative_url}}" />
  {%- endif -%}
{%- endfor -%}
</h2>

* Postdoctoral Researcher  
* Biozentrum, University of Basel

<!--more-->

* email: [alexander.kanitz@unibas.ch](mailto:alexander.kanitz@unibas.ch)
* web: [Biozentrum](http://www.biozentrum.unibas.ch/)
