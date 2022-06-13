---
title: "Human Copy Number Variation community"
layout: default
date: 2019-06-05
permalink: /index.html
author: "@mbaudis"
category:
  - general
tags:
---

## {{page.title}}

The [website](http://hcnv.github.io) of the _Human Copy Number Variation Community_ (hCNV) is a resource originating in ELIXIR's h-CNV Community Implementation Study (2019-2021).

Genomic variants are the basis of individual variations in human phenotypes and susceptibility to a large variety of diseases. Inherited variants can be the cause for syndromic or "rare" diseases, while neoplastic diseases ("cancer") arise from the accumulation of genomic variants in body tissues ("somatic mutations"), during the lifetime of an individual but sometimes associated with pre-disposing, inherited genome variations.

<img style="float: right; width: 200px; margin-left: 15px; margin-bottom-10px;" src="/assets/img/9p-example-histogram.png" />Among the different types of inherited and acquired genomic variants, regional genomic copy number variations (CNV) contribute - if measured by affected genomic sequences - contribute by far the largest amount of genomic changes, contributing both to many syndromic diseases as well as the vast majority of human cancers. These CNVs act through modifications of the dosage of genomic elements away from the base copy number, from the total abrogation of genetic function in homozygous deletions to genetic hyperactivity by copy number amlifications, sometimes resulting in tens or hundreds of copies of disease related genes.

Despite the fact that Copy Number Variations are the most prevalent genetic mutation type, identifying and interpreting them still represents a major challenge. The ELIXIR human Copy Number Variation (hCNV) Community aims to implement processes to facilitate the detection, annotation and interpretation of these variations, and to engage scientists, clinicians and industry partners with significant involvement in areas relevant to the community.

### Latest News    

{% comment %}
	Some news ...
{% endcomment %}


{%- assign this_name = "news" -%}
{%- assign this_category = "news" -%}
{%- assign max_list = 3 -%}
{%- assign count_list = 0 -%}

{%- assign cat_posts = site.emptyArray -%}
{%- for post in site.documents -%}
  {%- if post.categories contains this_category -%}
    {%- assign cat_posts = cat_posts | push: post -%}
  {%- endif -%}
{%- endfor -%}

{%- assign cat_posts = cat_posts | sort: 'date' | reverse -%}

{% for post in cat_posts limit: max_list %}
  {% unless post.tags contains '.prepend' or post.tags contains '.append' %}
    {%- assign post_author = post.author | downcase -%}
    {%- assign excerpt_link = post.url | relative_url -%}
    {%- if post.excerpt_link contains '/' -%}
      {%- assign excerpt_link = post.excerpt_link -%}
    {%- endif -%}
<div class="excerpt">
<a href="{{ excerpt_link }}">{{ post.excerpt }}</a>
  <p class="footnote">
    {%- if post.author -%}{{ post.author | join: " | " }}&nbsp;{%- endif -%}
    {%- if post.date -%}{{ post.date | date: "%Y-%m-%d" }}: {% endif %}
 <a href="{{ excerpt_link }}">more ...</a>
  </p>
</div>
  {% endunless %}  
{% endfor %}

{% comment %}
	More static content ...
{% endcomment %}
