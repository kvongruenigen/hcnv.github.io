---
title: "BANCCO - Banque Nationale de CNV Constitutionnelles"
layout: default
date: 2018-07-01
excerpt_separator: <!--more-->
excerpt_link: 'https://bancco.fr'
www_link:
www_links_formatted:
image_file: 'bancco-logo-180.png'
category:
  - resources
tags: # please delete unneeded options
  - databases
  - tools
---

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; " src="{{ static_file.path | relative_url}}" />
  {% endif %}
{% endfor %}

## {{page.title}}

La banque nationale de CNV Constitutionnelles est développée afin de recenser 
les CNV (Copy Number Variation) issus du diagnostic clinique.

<!--more-->

