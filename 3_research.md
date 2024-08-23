---
layout: page
title: "Research"
description: "evolutionary and population genetics"
header-img: "img/received_1325138571544423.jpeg"
---

### Ongoing

#### Incorporating long-distance migration events onto existing migration surfaces

(empirical/methods development) As part of a summer rotation, I was involved in incorporating long-distance migration events into the existing [FEEMS](https://github.com/NovembreLab/feems) software from the Novembre lab. This project has since blossomed into a full chapter in my thesis, with the development of a novel method called `FEEMSmix` for representing long-range genetic similarity on a background effective migration map estimated by `FEEMS`. This work follows on previous work like [TreeMix](https://dx.plos.org/10.1371/journal.pgen.1002967) (and, to a certain extent, [SpaceMix](https://dx.plos.org/10.1371/journal.pgen.1005703)) in modeling residuals from underlying fits as admixture events. 

Poster for Evolution 2023 can be found here <a href="/docs/Evolution_2023.pdf" target="_blank"><i class="fa fa-file-text fa-md"></i></a>.  
Software for the methods can be cloned from here: [https://github.com/VivaswatS/feems/tree/main](https://github.com/VivaswatS/feems/tree/main) (*subject to change*)

#### Estimating selection on genealogies 

(methods development) As an extension to our previous method for computing the density on ages, we also formulate a model to infer selection on the derived allele using the estimated tree at a given site, conditional on the age of the mutation. This is very similar to [CLUES](https://doi.org/10.1371/journal.pgen.1008384) in its functionality (in fact, we observe similar error rates in simualtions), but using quite a different framework inspired by the Ancestral Selection Graph (ASG, Neuhauser & Krone 1997). This is still a work in progress, but with potential to incorporate more general demographic models like a split-population scenario with migration.  

Poster for ProbGen 2024 can be found here <a href="/docs/ProbGen_2024.pdf" target="_blank"><i class="fa fa-file-text fa-md"></i></a>. 

### Previous 


#### Improving DFE estimation with paired data of allele frequency and allele age

(theoretical/simulations) Estimating the fitness effect of de-novo mutations is an important problem in population and evolutionary genetics. The accurate estimation of the distribution of fitness effects (DFE) is crucial in understanding a broad variety of processes, from selection shaping genetic diversity in natural populations to the evolution of complex traits in the human population. Typically, DFE estimation is done using the allele frequency information from the site frequency spectrum (SFS), but we propose using paired data of allele age and allele frequency as this gives us more information about the trajectory and selection pressure on the *de-novo* mutation. We find that using this paired data helps us estimate selection coefficients in simulated data with slightly higher certainty than using allele frequency alone, but only in some cases. As part of this project, we also provide a fast way to compute the expecteed density on age given a sample frequency and selection coefficient (under any demographic history). 

Poster for ProbGen 2023 can be found here <a href="/docs/ProbGen_2023.pdf" target="_blank"><i class="fa fa-file-text fa-md"></i></a>.   
Work detailing the results can be found in this [preprint](https://doi.org/10.1101/2024.08.06.606888). 

#### Estimating genotype and ancestry in hybrids of mixed-ploidy 

(methods development) As part of my MS thesis, I worked on extending a hierarchical Bayesian model presented in [Gompert et al, 2014](https://cpb-us-e1.wpmucdn.com/wp.txstate.edu/dist/a/171/files/2013/05/gompert14.pdf) to run with mixed-ploidy species. The model uses genotype-likelihood data to estimate parameters like genotype and ancestry, similar to the [structure](https://web.stanford.edu/group/pritchardlab/structure.html) software, with application to low-coverage sequencing data. The software is written in C++ with the use of GSL and HDF5 libraries. Using this model, we show that [entropy](https://bitbucket.org/buerklelab/mixedploidy-entropy/src/master/) provides finer resolution in admixture proprotion estimates in a diploid-tetraploid hybrid zone of *Arabadopsis arenosa* in central Europe compared to the current standard. 

#### Quantifying genetic diversity of *Wolbachia* in *Lycaeides* populations

(empirical) *Wolbachia* is an endosymbiotic bacteria that is found in a majority of all insect species and its infection leads to a variety of detrimental phenotypic effects to the population biology of its hosts. However, infection dynamics across species ranges are largely under studied. In this study, we used GBS data from 2388 host butterflies from 109 populations across the United States to quantify the rate and mode of infection in our system using a bioinformatics approach. We find that most of our populations have very high rates of infection (mean = 91%) and that there are three major strains of *Wolbachia* infecting our butterfly species. More information in this [preprint](https://www.authorea.com/doi/full/10.22541/au.164703040.01856976/v1). 

#### Modeling differential abundance testing in microbial count data

(methods development) As part of a lab project to quantify differential abundance in microbial count data, I ported code to model microbial (and ecological) count data to Hamiltonian MC with Stan. This led to faster and more accurate results than the previously used method with Gibbs sampling in JAGS. The model is written into an R package [CNVRG](https://rdrr.io/github/JHarrisonEcoEvo/CNVRG/) that takes as input an OTU table from different treatments (for example, case and control) and fits a Dirichlet-Multinomial conjugate distribution to these two data sets. The ditribution of parameter estimates for the frequencies of the microbes in the two groups are output, after which the question of whether their abundance is different between the two treatments can be answered with a more parametric basis. 
