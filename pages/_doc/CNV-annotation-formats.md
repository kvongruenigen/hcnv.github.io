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
---

## {{page.title}}

<!--more-->

### ISCN

##### Links

* ISCN 2016 is the latest edition, available as book (Karger)


### HGVS

##### Links

* HGVS DNA [Sequence Variant Nomenclature](http://varnomen.hgvs.org/recommendations/DNA/)


### VCF

While VCF is a file format, originally developed (and optimised) for the 
representation of possibly recurring variants across a set of analyses, it also
allows for the storage & representation of CNV events.

##### Links

* VCF specification [v4.2 PDF](https://samtools.github.io/hts-specs/VCFv4.2.pdf)


### Variant Schemas

#### GA4GH "Variant Representation" schema

The "Genomic Knowledge Standards" (GKS) of the Global Alliance for Genomics and
Health [GA4GH](http://ga4gh.org) develops a modern schema for the unambiguous
representation, transmission and recovery of sequence variants (genomic and
beyond).

The first release of the [GA4GH Variation Representation Specification
([vr-spec v1.0](https://github.com/ga4gh/vr-spec/releases/tag/1.0.0))
does not yet include the option to represent structural variants. However, the
internal roadmap of the project points towards an extension for CNV 
representation in 2020.

##### Links

* _vr-spec_ [repository](https://github.com/ga4gh/vr-spec)
* [documentation](https://vr-spec.readthedocs.io/en/1.0/)


#### GA4GH Data Working Group schema (deprecated)

The original GA4GH `Variant` schema was essentially a rewritten version of parts
of the VCF specification into an object model.

##### Links

* `Variant` documentation for the [GA4GH schema](https://ga4gh-schemas.readthedocs.io/en/latest/schemas/variants.proto.html#protobuf.Variant)
* Protobuf version of the `Variant` object in the (deprecated) [GA4GH schema](https://github.com/ga4gh/ga4gh-schemas/blob/master/src/main/proto/ga4gh/variants.proto#L145)


### Ad-Hoc & "Community" Formats

#### _Progenetix_ `Variant` schema

The [Progenetix](http://progenetix.org) cancer genome profiling resource (and 
the) sister project [arrayMap](http://arraymap.org) store their millions of CNVs
in as data objects in [MongoDB](http://mongodb.org) document databases. The 
format of the single variants is based on the original GA4GH schema (see above),
with some extensions and modifications.

Development of the _Progenetix_ format closely follows the work of the GA4GH GKS
group and is expected, over time, to adopt core objects and concepts from
_vr-spec_ [repository](https://github.com/ga4gh/vr-spec).

##### Progenetix CNV example

```
{
	"_id" : ObjectId("5c865b9509d374f2dc2c7cb3"),
	"callset_id" : "pgxcs::GSE10007::GSM252886",
	"digest" : "1:911484-11993973:DEL",
	"variantset_id" : "AM_VS_GRCH38",
	"biosample_id" : "PGX_AM_BS_GSM252886",
	"reference_name" : "1",
	"variant_type" : "DEL",
	"start" : [
		911484
	],
	"end" : [
		11993973
	],
	"info" : {
		"provenance" : "arraymap import",
		"cnv_value" : -0.3933,
		"cnv_length" : 11082489
	}.
	"updated" : "2018-12-06 11:17:17.485238"
}
```

##### Links

* schema in _progenetix/schemas_ [code repository](https://github.com/progenetix/schemas/blob/master/main/yaml/variant.yaml)


