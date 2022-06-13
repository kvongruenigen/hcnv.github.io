---
title: CNV Annotation Formats
description: Some Information about CNV Annotation Standards
date: 2019-12-12
authors:
  - "@mbaudis"
---

## ISCN

Sine 1963, the _International System for Human Cytogenetic Nomenclature_ (ISCN) has provided standards and guidelines for annotation of human karyotypes and cytogenetic abnormalities.

<!--more-->

Recent editions have tried to accomodate for genomic variants derived from
molecular and molecular-cytogenetics technologies such as FISH, genomic
microarrays and DNA sequencing.

#### Examples (CNV)

* `46,XX,trp(8)(q21q24)`
* `ish cgh dim(17p12p11),enh(8)(q24)`
    - chromosomal Comparativ Genomic Hybridization (CGH)

#### Links

* ISCN 2016 is the latest edition, available as book (Karger)

## HGVS

#### Links

* HGVS DNA [Sequence Variant Nomenclature](http://varnomen.hgvs.org/recommendations/DNA/)


## VCF

While VCF is a file format, originally developed (and optimised) for the
representation of possibly recurring variants across a set of analyses, it also
allows for the storage & representation of CNV events.

#### Links

* VCF specification [v4.2 PDF](https://samtools.github.io/hts-specs/VCFv4.2.pdf)


## Variant Schemas

### GA4GH "Variant Representation" schema

The "Genomic Knowledge Standards" (GKS) of the Global Alliance for Genomics and
Health [GA4GH](http://ga4gh.org) develops a modern schema for the unambiguous
representation, transmission and recovery of sequence variants (genomic and
beyond).

The first release of the [GA4GH Variation Representation Specification
([vr-spec v1.0](https://github.com/ga4gh/vr-spec/releases/tag/1.0.0))
does not yet include the option to represent structural variants. However, the
internal roadmap of the project points towards an extension for CNV
representation in 2020.

#### Links

* _vr-spec_ [repository](https://github.com/ga4gh/vr-spec)
* [documentation](https://vr-spec.readthedocs.io/en/1.0/)


## Ad-Hoc & "Community" Formats

### _Progenetix_ `Variant` schema

The [Progenetix](http://progenetix.org) cancer genome profiling resource store their millions of CNVs
in as data objects in [MongoDB](http://mongodb.org) document databases. The
format of the single variants is based on the original GA4GH schema (see above),
with some extensions and modifications.

Development of the _Progenetix_ format closely follows the work of the GA4GH GKS group adopts core objects and concepts from
_vr-spec_ [repository](https://github.com/ga4gh/vr-spec).

The _Progenetix_ data serves as the repository behind the
[Beacon<span style="color: red; font-weight: 800;">+</span>](http://beacon.progenetix.org) forward looking implementation of the [ELIXIR Beacon](http://beacon-project.io) project.

#### Progenetix CNV example

```
{
  _id: ObjectId("5bab576a727983b2e00b8d32"),
  id: 'pgxvar-5bab576a727983b2e00b8d32',
  variant_internal_id: '11:52900000-134452384:DEL',
  callset_id: 'pgxcs-kftvldsu',
  biosample_id: 'pgxbs-kftva59y',
  individual_id: 'pgxind-kftx25eh',
  variant_state: { id: 'EFO:0030067', label: 'copy number loss' },
  type: 'RelativeCopyNumber',
  location: {
    sequence_id: 'refseq:NC_000011.10',
    type: 'SequenceLocation',
    interval: {
      start: { type: 'Number', value: 52900000 },
      end: { type: 'Number', value: 134452384 }
    }
  },
  relative_copy_class: 'partial loss',
  updated: '2022-03-29T14:36:47.454674'
}
```

#### Links

* schema in _progenetix/bycon_ [code repository](https://github.com/progenetix/bycon/blob/master/schemas/src/progenetix-database-schemas/pgxVariant.yaml)
