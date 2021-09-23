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

## {{page.title}}

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; width: 80px; margin-top: -30px; margin-right: 10px;" src="{{ static_file.path | relative_url}}" />
  {%- endif -%}
{%- endfor -%}

Postdoctoral Researcher  
Biozentrum, University of Basel

<!--more-->

* email: [alexander.kanitz@unibas.ch](mailto:alexander.kanitz@unibas.ch)
* web: [Biozentrum](http://www.biozentrum.unibas.ch/)
