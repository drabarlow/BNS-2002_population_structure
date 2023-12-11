---
title       : "Population structure"
subtitle    : "BNS-2002: Genes, Development, and Evolution"
author      : Dr Axel Barlow
job         : "email: a.barlow@bangor.ac.uk"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : zenburn      # {zenburn, tomorrow, solarized-dark, ...}
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {selfcontained, standalone, draft}
knit        : slidify::knit2slides
logo        : LA_Full_colour_reversed.svg
biglogo     : A1_FullColour.svg
assets      : {assets: ../../assets}
license     : by-nc-sa

---



<!-- adding bold and italic options -->
<style>
em {
  font-style: italic
}
strong {
  font-weight: bold;
}
</style>

## Phylogenetics and population genetics lectures

- Key concepts and Single locus phylogenetics
- Multi-locus phylogenetics
- **Population structure**
  - **Theory**
  - **Methods**
  - **Discoveries**
- Conservation genetics

---

## How does the tree form: lineage sorting

<img src="./assets/img/linsort1.svg" width="100%" style="display: block; margin: auto;" />

---

## How does the tree form: lineage sorting

<img src="./assets/img/linsort2.svg" width="100%" style="display: block; margin: auto;" />

---

## How does the tree form: lineage sorting

<img src="./assets/img/linsort3.svg" width="100%" style="display: block; margin: auto;" />

---

## How does the tree form: lineage sorting

<img src="./assets/img/linsort4.svg" width="100%" style="display: block; margin: auto;" />

---

## How does the tree form: lineage sorting

<img src="./assets/img/linsort5.svg" width="100%" style="display: block; margin: auto;" />

---

## Population structure

- Phylogenetic approaches less suited to recent population divergence events
- Insufficient time for lineage sorting
- After population isolation, allele frequencies in subpopulations will diverge under drift
- Differences in allele frequencies provide a way of identifying populations and measuring their divergence
- The extent of structuring depends on the magnitude of drift and gene flow
- Structure can still persist with low level gene flow

---

## Simulator

<iframe src = 'https://www.whfreeman.com/BrainHoney/Resource/6716/SitebuilderUploads/Hillis2e/Student%20Resources/Animated%20Tutorials/pol2e_at_1502_genetic_drift_simulation/pol2e_at_1502_genetic_drift_simulation.html' height='600px'></iframe>

---

## Why is it important?

### Populations play a central role in:
  - Evolution
  - Ecology
  - Conservation

### We need to know:
  - How many populations there are
  - Where do they occur spatially
  - How divergent are they
  - Do they exchange migrants

--- .segue .dark 

## Population structure - methods

---

## Getting the data

### Data is almost always multilocus. Many approaches have been and gone

- RAPDs
- RFLPs
- AFLPs
- Microsatellites

### Current methods are all single nucleotide polymorphism (SNP) based

- RADseq
- SNP array capture
- Whole genome resequencing

---

## Fst

Ht = expected* heterozygosity in total population

Hs = average expected* heterozygosity within subpopulations

*under HWE expectations

### **Fst = Ht - Hs /  Ht**

- Based on allele frequencies
- Measures change in expected heterozygosity for subpopulations vs a single (big) population
- Ranges from 0 (no subpopulations) to 1 (subpopulations fixed for different alleles)
- Indicates proportion of total variation structured between subpopulations
- Also useful for detecting selection

---

## Fst

<img src="./assets/img/fst1.svg" width="100%" style="display: block; margin: auto;" />

---

## Fst

<img src="./assets/img/fst2.svg" width="100%" style="display: block; margin: auto;" />

---

## Fst

<img src="./assets/img/fst3.svg" width="100%" style="display: block; margin: auto;" />

--- &twocol

## Principal components analysis (PCA)

*** =left

- used for decades, modern implementation introduced in 2006
- Analysis of individuals
- Used allele variance relative to average
- model free (does not assume populations)
- Input is individual genotypes
- PCA find a single continuous variable that explains largest proportion of the variation (PC1)
- PC2 explains largest proportion not explained by PC1, etc...
- Allows exploration of where the populations are

*** =right

<img src="assets/fig/unnamed-chunk-9-1.png" width="100%" style="display: block; margin: auto;" />

---

## STRUCTURE

- Introduced in 2000
- NGSadmix is STRUCTURE adapted for whole genome data
- User tells program the number of populations (K)
- Input is individual genotypes
- STRUCTURE assigns individuals to K populations maximising Hardy-Weinberg and linkage equillibrium
- Also allows individuals to be admixed
- Major challenge is determining K: either need strong prior knowledge, or test a range

--- &vcenter

## STRUCTURE example

<img src="./assets/img/Map_of_samples_and_population_structure_of_North_Africa_and_neighboring_populations.png" width="100%" style="display: block; margin: auto;" />

--- .segue .dark 

## Population structure: discoveries

--- &twocol

## Hooded and carrion crows

*** =left

<img src="./assets/img/Nebelkrähe_Corvus_cornix,_Belvedere,_Wien.jpg" width="100%" style="display: block; margin: auto;" />

*** =right

<img src="./assets/img/Distribution_of_carrion_and_hooded_crows_across_Europe.jpg" width="100%" style="display: block; margin: auto;" />

---

## Genome-wide Fst

<img src="./assets/img/cro.png" width="100%" style="display: block; margin: auto;" />

---

## Crow reading

<embed src="./assets/img/1111crow410.full.pdf" width="100%" height="500" type="application/pdf" />


--- &twocol

## Leopards

*** =left

- Most widely distributed big cat
- Fossil record indicates African origin
- No range wide population genetics study
- 26 museum and modern genomes
- 8 subspecies, more or less supported by mtDNA
- African plus 7 Asian subspecies

*** =right

<img src="./assets/img/leopard_map.svg" width="100%" style="display: block; margin: auto;" />

<img src="./assets/img/drawing.svg" width="80%" style="display: block; margin: auto;" />

--- &twocol

## Leopards

*** =left

<img src="./assets/img/leopard_pca.svg" width="100%" style="display: block; margin: auto;" />

*** =right

<img src="./assets/img/leopard_map.svg" width="100%" style="display: block; margin: auto;" />

<img src="./assets/img/drawing.svg" width="80%" style="display: block; margin: auto;" />

--- &twocol

## Leopards

*** =left

<img src="./assets/img/leopard_struct.svg" width="100%" style="display: block; margin: auto;" />

*** =right

<img src="./assets/img/leopard_map.svg" width="100%" style="display: block; margin: auto;" />

<img src="./assets/img/drawing.svg" width="80%" style="display: block; margin: auto;" />

---

## Leopard reading

<embed src="./assets/img/Paijmans et al. - 2021 - African and Asian leopards are highly differentiated at the genomic level.pdf" width="100%" height="500" type="application/pdf" />

--- &twocol

## Tiger sharks

*** =left

- Oceanic shark
- Apex predator, ecologically flexible
- Global distribution
- Some show seasonal migration
- Can move 1000's km

*** =right

<img src="./assets/img/Tiger-Shark-Pictures.jpg" width="100%" style="display: block; margin: auto;" />

--- bg:white

## Tiger sharks

<img src="./assets/img/tiger_str.svg" width="100%" style="display: block; margin: auto;" />

<img src="./assets/img/tiger_map.svg" width="85%" style="display: block; margin: auto;" />

---

## Tiger shark reading

<embed src="./assets/img/esab046.pdf" width="100%" height="500" type="application/pdf" />

--- &twocol

## Giraffes

*** =left

- Confused subspecies taxonomy
- Nine subspecies more or less accepted
- Overall listed as vulnerable by IUCN
- Some subspecies are critically endangered

*** =right

<img src="./assets/img/800px-Rothschild's_Giraffe_(Giraffa_camelopardalis_rothschildi)_male_(7068054987),_crop_&_edit.jpg" width="80%" style="display: block; margin: auto;" />

---

## Four giraffe species?

<embed src="./assets/img/Fennessy et al. - 2016 - Multi-locus Analyses Reveal Four Giraffe Species Instead of One.pdf" width="100%" height="500" type="application/pdf" />

---

## Four giraffe species?

<embed src="./assets/img/Bercovitch et al. - 2017 - How many species of giraffe are there.pdf" width="100%" height="500" type="application/pdf" />

--- &twocol

## Giraffes

*** =left

<img src="./assets/img/giraffe_map.svg" width="100%" style="display: block; margin: auto;" />

*** =right

<img src="./assets/img/giraffe_pca.svg" width="100%" style="display: block; margin: auto;" />

--- &twocol

## Giraffes

*** =left

<img src="./assets/img/giraffe_map.svg" width="100%" style="display: block; margin: auto;" />

*** =right

<img src="./assets/img/giraffe_stru.svg" width="100%" style="display: block; margin: auto;" />

---

## Giraffes

<img src="./assets/img/giraffe_fin.svg" width="100%" style="display: block; margin: auto;" />

---

## Giraffe reading

<embed src="./assets/img/giraffe.pdf" width="100%" height="500" type="application/pdf" />

--- &thankyou

## Next time

**Conservation genetics**





