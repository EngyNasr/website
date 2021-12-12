---
site: freiburg
tags:
title:
  Accessible and scalable detection and identification of foodborne pathogens, a
  project with Biolytix and funded by EOSC-Life
supporters:
  - eosc
  - biolytix
  - elixir
  - denbi
---

**TLDR**: Thanks to funding from [EOSC-Life](https://www.eosc-life.eu/), the
Freiburg Galaxy team will work in 2022 with
[Biolytix](https://www.biolytix.ch/en/), a Swiss Small and Medium-sized
Enterprise (SME) specialized in molecular biology and microbiological analyses,
toward **Accessible and scalable detection and identification of foodborne
pathogens**.

## Background

Food contaminations with pathogens are a major burden on our society. In the
year 2019, foodborne pathogens caused 137 diseases in Germany (BVL 2019).
Globally, they affect an estimated 600 million people a year and impact
socioeconomic development at different levels. These outbreaks are mainly due to
_Salmonella_ spp. followed by _Campylobacter_ spp. and Noroviruses.

During the investigation of a foodborne outbreak, a microbiological analysis of
the probable responsible food vehicle is performed in order to detect the
responsible pathogens and track the contamination source. By default, to detect
bacterial pathogens in food, the European Regulation (CE) follows ISO standards,
but alternative methods with equivalent performance are possible. Usually,
foodborne pathogens are detected and identified by stepwise cultures on
selective media and/or targeting specific genes with real-time PCRs. To
characterize the detected strains, the current gold standard is Pulsed-field Gel
Electrophoresis (PFGE) or Multiple-Locus Variable Number Tandem Repeat Analysis
(MLVA). These techniques have some disadvantages. Whole Genome Sequencing (WGS)
has been proposed as an alternative:

- detection of all genes with just one sequencing run,
- phylogenetic analysis to link cases,
- information on antimicrobial resistance genes, virulence, serotype, resistance
  to sanitizers, root cause, and other critical factors in one assay, including
  historical reference to pathogen emergence.

WGS is more than a surveillance tool and was recommended by the European Centre
for Disease Prevention and Control (ECDC) and the European Food Safety Authority
(EFSA) for surveillance and outbreak investigation. WGS still requires isolation
of the targeted pathogen, which is a time-consuming, not always straightforward
nor successful process. Sequencing methods without prior isolation could solve
this issue.

The evolution of sequencing techniques in the last decades has made possible the
development of shotgun metagenomic sequencing, i.e. the direct sequencing of all
DNA present in a sample. This approach gives an overview of the genomic
composition of all cells in the sample, including the food source itself, the
microbial community and any possible pathogens and their complete genetic
information, without the need for prior isolation. Several studies have
demonstrated the potential of shotgun metagenomics to identify and characterize
pathogens and their functional characteristics (e.g. virulence genes) in
naturally contaminated or spiked food samples.

The currently available studies used Illumina sequencing, generating short
reads. Longer read lengths, generated by third generation sequencing platforms
such as Pacific Biosciences (PacBio) and Oxford Nanopore Technologies (ONT),
make it easier and more practical to identify strains with fewer reads. MinION
(from Oxford Nanopore) is a portable, real-time device for ONT sequencing.
Several proof-of-principle studies have shown the utility of ONT long read
sequencing from metagenomic samples for pathogen identification.

## Our project

The industry partner of this project, [Biolytix](https://www.biolytix.ch/en/),
is a Swiss Small and Medium-sized Enterprise (SME) founded in 1998, that
specializes in molecular biology and microbiological analyses. They developed a
procedure to extract, sequence using MinION (ONT) sequencing and analyze a food
sample for foodborne pathogen detection and contamination source tracking.
However, the bioinformatics pipelines are not following the best practices for
open data science, not straightforward and can only be manipulated by the
original author, making it not scalable.

The aim of the project is to **modernize, FAIRify and validate the bioinformatic
pipeline developed by Biolytix to extract, sequence using MinION (ONT)
sequencing and analyze a food sample for foodborne pathogen detection and
contamination source tracking using modern paradigms of data science to make it
accessible and scalable.**

What do we plan to do?

1. Version, document and package the manual tasks and custom scripts into proper
   tools;
2. Replace some tools by state-of-the-art and open-source and free to use tools;
3. Improve dependency resolution by providing
   [Bioconda](https://bioconda.github.io/)/[Biocontainer](https://biocontainers.pro/)
   for all tools;
4. Update and version databases;
5. Migrate to an explicit workflow environment system (Galaxy):
   1. Update existing wrappers and create new wrappers when needed for all tools
      and share them on the [Galaxy ToolShed](https://toolshed.g2.bx.psu.edu/),
   2. Associate all databases to data managers and add them to Galaxy
      [CVMFS](https://cernvm.cern.ch/fs/),
   3. Add proper visualization,
   4. Add automatic report generation;
   5. Annotate tools and workflows with metadata including
      [ELIXIR bio.tools](https://bio.tools/);
6. Validate the workflows:
   1. Blind tests on the data generated by Biolytix,
   2. Comparison with results from existing workflow;
7. Develop a suite for automatic workflow tests and integrate it with
   [EOSC-Life Life-Monitor](https://lifemonitor.eu/)
8. Share the workflows on [IWC](https://github.com/galaxyproject/iwc) and
   [EOSC-Life Workflow Hub](https://workflowhub.eu/);
9. Documentation in the form of online tutorials in the
   [Galaxy Training Network](https://training.galaxyproject.org/);
10. Organization of a workshop;
11. Dissemination and advertisement of the workflows to interested (industry)
    parties.