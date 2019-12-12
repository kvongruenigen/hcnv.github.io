---
title:  "CNV Annotation Formats"
permalink: /doc/CNV-annotation-formats.html
layout: default
date:   2019-12-12
author: "@mbaudis"
excerpt_link: 
excerpt_separator: <!--more-->
category:
  - standards
tags:
  - standards
  - files
  - standards
---

## {{page.title}}



### ISCN

* ISCN 2016 is the latest edition, available as book (Karger)


### HGVS

* HGVS Sequence Variant Nomenclature [&nearr;](http://varnomen.hgvs.org)


### VCF

While VCF is a file format, originally developed (and optimised) for the 
representation of possibly recurring variants across a set of analyses, it also
allows for the storage & representation of CNV events.

* VCF specification [v4.2 PDF &nearr;](https://samtools.github.io/hts-specs/VCFv4.2.pdf)



### Variant Schemas

The original GA4GH `Variant` schema was essentially a rewritten version of parts
of the VCF specification into an object model.

* `Variant` documentation for the (deprecated) GA4GH schema [&nearr;](https://ga4gh-schemas.readthedocs.io/en/latest/schemas/variants.proto.html#protobuf.Variant)
* Protobuf version of the `Variant` object in the (deprecated) GA4GH schema [&nearr;](https://github.com/ga4gh/ga4gh-schemas/blob/master/src/main/proto/ga4gh/variants.proto#L145)



### Ad-Hoc & "Community" Formats
