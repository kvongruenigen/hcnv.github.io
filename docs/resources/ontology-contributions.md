---
title: "CNV-related contributions to ontologies"
description: h-CNV Community Members and their Involvement with Classifications and Ontologies
template: post.html
date: 2022-01-06
authors:
  - "@mbaudis"
---

h-CNV community members have been contributors to several ontologies, for the
representation of technologies relevant for CNV analysis as well as for the
encoding of CNV data.

## Ontology of bioscientific data analysis and data management (EDAM)

* [Copy number variation detection](http://edamontology.org/operation_3961) and
child terms
  - contributed by David Salgado

## Experimental Factor Ontology (EFO)

### Genomic array types

Terms for genomic array types used in CNV detection were added to the existing
[DNA array](http://www.ebi.ac.uk/efo/EFO_0002701) concept (Michael Baudis):
<!--more-->

* large-insert clone DNA microarray ([EFO:0010938](http://www.ebi.ac.uk/efo/EFO_0010938))
* oligonucleotide DNA microarray ([EFO:0010939](http://www.ebi.ac.uk/efo/EFO_0010939))
* SNP array ([EFO:0002703](http://www.ebi.ac.uk/efo/EFO_0002703))
  - the term existed but was re-assigned as child of EFO:0010939
* oligonucleotide DNA microarray ([EFO:0010939](http://www.ebi.ac.uk/efo/EFO_0010939))

### Relative copy number changes

For many practical purposes CNVs should be represented as one from a limited set
of conceptual, relative copy number classes. Here - together with members of the
[GA4GH VRS team](https://github.com/ga4gh/vrs/issues/277) - have developed a hierarchical mini classification which can be
referred to using the Experimental Factor Ontology terms (see also 2022 [proposal](https://github.com/EBISPOT/efo/issues/1404) for adding a subtree to EFO and/or SO for the representation of relative CNV
values).

* [`copy number assessment`](https://www.ebi.ac.uk/ols4/ontologies/efo/classes/http%253A%252F%252Fwww.ebi.ac.uk%252Fefo%252FEFO_0030063) subtree at EFO in OLS
* documentation of the [term use in different standards](/resources/CNV-annotation-standards/)

```
id: EFO:0030063
label: copy number assessment
  |
  |-id: EFO:0030064
  | label: regional base ploidy
  |   |
  |   \-id: EFO:0030065
  |     label: copy-neutral loss of heterozygosity
  |
  \-id: EFO:0030066
    label: relative copy number variation
      |
      |-id: EFO:0030067
      | label: copy number loss
      |   |
      |   |-id: EFO:0030068
      |   | label: low-level copy number loss
      |   |
      |   |-id: EFO:0020073
      |     label: high-level copy number loss
      |     note:  >-
      |       preferred in contrast to EFO:0030069 when a complete loss of all alleles
      |       at an indicated position cannot be reasonably assessed
      |       |
      |       \-id: EFO:0030069
      |         label: complete genomic deletion
      |
      |-id: EFO:0030070
        label: copy number gain
          |
          |-id: EFO:0030071
          | label: low-level copy number gain
          |
          \-id: EFO:0030072
             label: high-level copy number gain
             note: commonly but not consistently used for >=5 copies on a bi-allelic genome region
              |
              \-id: EFO:0030073
                 label: focal genome amplification
                 note: >-
                   commonly used for localized multi-copy genome amplification events where the
                   region does not extend >3Mb (varying 1-5Mb) and may exist in a large number of
                   copies

```

## Sequence Ontology (SO)

As of 2023-05-19 the request for a clear CNV class handling hasn't been progressed
at SO. Please feel free to ping there! However, we now recommend using the EFO terms
linked above (or their equivalent reprersentation in the GA4GH VRS standard from 
version 1.3 onward).

* SO copy number assessment subtree proposal [on Github](https://github.com/The-Sequence-Ontology/SO-Ontologies/issues/568)



---
 
Last update: 2023-05-19



