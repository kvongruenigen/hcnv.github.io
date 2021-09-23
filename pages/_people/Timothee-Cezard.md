---
title: "Timothee Cezard"
layout: default
image_file: 'tcezard.jpg'
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

* EMBL-EBI  
* Project Lead - Keane team: European Genome-phenome Archive and European Variation Archive  

<!--more-->

* email: tcezard [at] ebi.ac.uk
* web: [ED Genomics](https://www.ebi.ac.uk/about/people/timothee-cezard)
* ORCID iD: [0000-0002-5626-270X](http://europepmc.org/search?query=AUTHORID:%220000-0002-5626-270X%22&sortby=Date)
