---
title: "CNV-related contributions to ontologies"
description: h-CNV Community Members and their Involvement with Classifications and Ontologies
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

Terms for genomic array types used in CNV detection were added to the existing
[DNA array](http://www.ebi.ac.uk/efo/EFO_0002701) concept (Michael Baudis):

* large-insert clone DNA microarray ([EFO:0010938](http://www.ebi.ac.uk/efo/EFO_0010938))
* oligonucleotide DNA microarray ([EFO:0010939](http://www.ebi.ac.uk/efo/EFO_0010939))
* SNP array ([EFO:0002703](http://www.ebi.ac.uk/efo/EFO_0002703))
  - the term existed but was re-assigned as child of EFO:0010939
* oligonucleotide DNA microarray ([EFO:0010939](http://www.ebi.ac.uk/efo/EFO_0010939))

There is also now (2022) a [proposal](https://github.com/EBISPOT/efo/issues/1404)
for adding a subtree to EFO and/or SO for the representation of relative CNV
values (see also below).

## Sequence Ontology (SO)

* SO copy number assessment subtree proposal [on Github](https://github.com/The-Sequence-Ontology/SO-Ontologies/issues/568)



