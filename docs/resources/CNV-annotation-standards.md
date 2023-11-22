---
title: CNV Annotation Formats
description: Some Information about CNV Annotation Standards
date: 2023-11-22
authors:
  - "@mbaudis"
---

## Cytogenetics vs. Molecular Biology...

With the "dual origin" in cytogenetics ("chromosome based") and genomics ("sequencing
based") analyses the annotation of copy number variants has evolved starting from
different directions. From the cytogenetic side the use of cytogenetic bands as
coordinate system, has been amended by increasing use of mapping positions (i.e.
for molecular-cytogenetic or hybrid analyses with known probe positions) while
for array and sequencing based CNV detection <!--more-->an increasing focus lies in the
determination of discrete allelic copy number counts and the assignment of a limited
set of CNV classes reflecting common use concepts.


## CNV Term Use Comparison in Computational (File/Schema) Formats

This table is maintained in parallel with the [Beacon v2 documentation](http://docs.genomebeacons.org/variant-queries/#term-use-comparison).
<!--more-->

| [EFO](http://www.ebi.ac.uk/efo/EFO_0030063) | Beacon | [VCF](https://samtools.github.io/hts-specs/) | SO       | GA4GH [VRS](https://vrs.ga4gh.org/en/latest/terms_and_model.html#copynumberchange)[^1] | Notes |
| ------------------------------------------- | ------------------------------------------------------------------------------ | -------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| <nobr>[`EFO:0030070`](http://www.ebi.ac.uk/efo/EFO_0030070)</nobr> copy number gain | `DUP`[^2] or<br/><nobr>[`EFO:0030070`](http://www.ebi.ac.uk/efo/EFO_0030070)</nobr> | `DUP`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001742`](http://www.sequenceontology.org/browser/current_release/term/SO:0001742) copy_number_gain | <nobr>[`EFO:0030070`](http://www.ebi.ac.uk/efo/EFO_0030070) gain  | a sequence alteration whereby the copy number of a given genomic region is greater than the reference sequence |
| [`EFO:0030071`](http://www.ebi.ac.uk/efo/EFO_0030071) low-level copy number gain| `DUP`[^2] or<br/><nobr>[`EFO:0030071`](http://www.ebi.ac.uk/efo/EFO_0030071)</nobr> | `DUP`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001742`](http://www.sequenceontology.org/browser/current_release/term/SO:0001742) copy_number_gain   | <nobr>[`EFO:0030071`](http://www.ebi.ac.uk/efo/EFO_0030071)</nobr> low-level gain |                                                                                                                             |
| [`EFO:0030072`](http://www.ebi.ac.uk/efo/EFO_0030072) high-level copy number gain | `DUP`[^2] or<br/><nobr>[`EFO:0030072`](http://www.ebi.ac.uk/efo/EFO_0030072)</nobr> | `DUP`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001742`](http://www.sequenceontology.org/browser/current_release/term/SO:0001742) copy_number_gain | <nobr>[`EFO:0030072`](http://www.ebi.ac.uk/efo/EFO_0030072)</nobr> high-level gain | commonly but not consistently used for >=5 copies on a bi-allelic genome region                                             |
| [`EFO:0030073`](http://www.ebi.ac.uk/efo/EFO_0030073) focal genome amplification  | `DUP`[^2] or<br/><nobr>[`EFO:0030073`](http://www.ebi.ac.uk/efo/EFO_0030073)</nobr> | `DUP`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001742`](http://www.sequenceontology.org/browser/current_release/term/SO:0001742) copy_number_gain | <nobr>[`EFO:0030072`](http://www.ebi.ac.uk/efo/EFO_0030072)</nobr> high-level gain[^4]  | commonly but not consistently used for >=5 copies on a bi-allelic genome region, of limited size (operationally max. 1-5Mb) |
| [`EFO:0030067`](http://www.ebi.ac.uk/efo/EFO_0030067) copy number loss            | `DEL`[^2] or<br/><nobr>[`EFO:0030067`](http://www.ebi.ac.uk/efo/EFO_0030067)</nobr> | `DEL`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001743`](http://www.sequenceontology.org/browser/current_release/term/SO:0001743) copy_number_loss | <nobr>[`EFO:0030067`](http://www.ebi.ac.uk/efo/EFO_0030067)</nobr> loss            | a sequence alteration whereby the copy number of a given genomic region is smaller than the reference sequence              |
| [`EFO:0030068`](http://www.ebi.ac.uk/efo/EFO_0030068) low-level copy number loss  | `DEL`[^2] or<br/><nobr>[`EFO:0030068`](http://www.ebi.ac.uk/efo/EFO_0030068)</nobr> | `DEL`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001743`](http://www.sequenceontology.org/browser/current_release/term/SO:0001743) copy_number_loss | <nobr>[`EFO:0030068`](http://www.ebi.ac.uk/efo/EFO_0030068)</nobr> low-level loss  |                                                                                                                             |
| [`EFO:0020073`](http://www.ebi.ac.uk/efo/EFO_0020073) high-level copy number loss  | `DEL`[^2] or<br/><nobr>[`EFO:0020073`](https://github.com/EBISPOT/efo/issues/1941)</nobr> | `DEL`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001743`](http://www.sequenceontology.org/browser/current_release/term/SO:0001743) copy_number_loss | <nobr>[`EFO:0020073`](https://github.com/EBISPOT/efo/issues/1941)</nobr> high-level loss  | a loss of several copies; also used in cases where a complete genomic deletion cannot be asserted |
| [`EFO:0030069`](http://www.ebi.ac.uk/efo/EFO_0030069) complete genomic deletion   | `DEL`[^2] or<br/><nobr>[`EFO:0030069`](http://www.ebi.ac.uk/efo/EFO_0030069)</nobr> | `DEL`<br/><nobr>`SVCLAIM=D`[^3]</nobr> | [`SO:0001743`](http://www.sequenceontology.org/browser/current_release/term/SO:0001743) copy_number_loss | <nobr>[`EFO:0030069`](http://www.ebi.ac.uk/efo/EFO_0030069)</nobr> complete genomic loss   | complete genomic deletion (e.g. homozygous deletion on a bi-allelic genome region)                                          |

##### Last updated 2023-03-22 by @mbaudis (VRS 1.3 adjustment)
##### updated 2023-03-22 by @mbaudis (EFO:0020073) & 2023-03-20 by @mbaudis (VRS proposal)

## ISCN

Sine 1963, the _International System for Human Cytogenetic Nomenclature_ (ISCN) has provided standards and guidelines for annotation of human karyotypes and cytogenetic abnormalities.

Recent editions have tried to accomodate for genomic variants derived from
molecular and molecular-cytogenetics technologies such as FISH, genomic
microarrays and DNA sequencing.

### Examples (CNV)

* `46,XX,trp(8)(q21q24)`
* `ish cgh dim(17p12p11),enh(8)(q24)`
    - chromosomal Comparativ Genomic Hybridization (CGH)

### Links

* ISCN 2020 is the latest edition, available as book (Karger)

## HGVS

### Links

* HGVS DNA [Sequence Variant Nomenclature](http://varnomen.hgvs.org/recommendations/DNA/)


## VCF

While VCF is a file format, originally developed (and optimised) for the
representation of possibly recurring variants across a set of analyses, it also
allows for the storage & representation of CNV events.

### Links

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

### Links

* _vr-spec_ [repository](https://github.com/ga4gh/vr-spec)
* [documentation](https://vr-spec.readthedocs.io/en/1.0/)


### Ad-Hoc & "Community" Formats

### _Progenetix_ `Variant` schema

The [Progenetix](http://progenetix.org) cancer genomics resource store their millions of CNVs
in as data objects in [MongoDB](http://mongodb.org) document databases. The
format of the single variants is based on the Beacon v2 default model with some
modifications (e.g. incorporating the VRS 1.3 `RelativeCopyNumber` concept but
w/ slightly rewrapped components).

The _Progenetix_ data serves as the repository behind the
[Beacon<span style="color: red; font-weight: 800;">+</span>](http://beaconplus.progenetix.org)
forward looking implementation of the [ELIXIR Beacon](http://beacon-project.io) project.
Accordingly, upon export through the API variants are re-mapped to a Beacon v2 representation.

#### Progenetix CNV example

```json
{
  "id": "pgxvar-5bab576a727983b2e00b8d32",
  "variant_internal_id": "11:52900000-134452384:DEL",
  "callset_id": "pgxcs-kftvldsu",
  "biosample_id": "pgxbs-kftva59y",
  "individual_id": "pgxind-kftx25eh",
  "variant_state": { "id": "EFO:0030067", "label": "copy number loss" },
  "type": "RelativeCopyNumber",
  "location": {
    "sequence_id": "refseq:NC_000011.10",
    "chromosome": "11",
    "type": "SequenceLocation",
    "interval": { "start": 52900000, "end": 134452384 }
    }
  }
  "updated": "2022-03-29T14:36:47.454674"
}
```

### Links

* schema in _progenetix/bycon_ [code repository](https://github.com/progenetix/bycon/blob/master/schemas/src/progenetix-database-schemas/pgxVariant.yaml)

[^1]: The VRS annotations refer to the status from v1.3 (2022) when 
the new class `CopyNumberChange` ([discussion...](https://github.com/ga4gh/vrs/issues/404#issuecomment-1472599849))
with the use of the EFO terms.
[^2]: While the use of VCF derived (`DUP`, `DEL`) values had been introduced with
beacon v1, usage of these terms has always been a _recommendation_ rather than an integral part
of the API. We now encourage the support of more specific terms (particularly EFO)
by Beacon developers. As example, the Progentix Beacon API [uses EFO terms](http://progenetix.org/search/) but
provides an internal term expansion for legacy `DUP`, `DEL` support.
[^3]: VCFv4.4 introduces an `SVCLAIM` field to disambiguate between _in situ_ events (such as
tandem duplications; known _adjacency_/ _break junction_: `SVCLAIM=J`) and events where e.g. only the
change in _abundance_ / _read depth_ (`SVCLAIM=D`) has been determined. Both **J** and **D** flags can be combined.
[^4]: VRS did not adopt the "amplification" term due to possible inconsistencies

