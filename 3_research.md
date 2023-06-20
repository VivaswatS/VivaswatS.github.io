---
layout: page
title: "Research"
description: "evolutionary and population genetics"
header-img: "img/brycecanyon.jpg"
---

### Ongoing

#### Improving DFE estimation with paired data of allele frequency and allele age

(theoretical/simulations) Estimating the fitness effect of de-novo mutations is an important problem in population and evolutionary genetics. The accurate estimation of the distribution of fitness effects (DFE) is crucial in understanding a broad variety of processes, from selection shaping genetic diversity in natural populations to the evolution of complex traits in the human population. Typically, DFE estimation is done using the allele frequency information from the site frequency spectrum (SFS), but we propose using paired data of allele age and allele frequency as this gives us more information about the trajectory and selection pressure on the *de-novo* mutation. We find that using this paired data helps us estimate selection coefficients in simulated data with slightly higher certainty than using allele frequency alone, but only in some cases. More insights to be had on this front... 

#### Incorporating long-distance migration events onto existing migration surfaces

(empirical/methods development) As part of a summer rotation, I was involved in incorporating long-distance migration events into the existing [feems](https://github.com/NovembreLab/feems) software from the Novembre lab. This involved adding long range edges (prompted by deviations to the fit) to a graph of migration rates inferred over the populations in 2-dimensional space. This was prompted by an empirical analysis of ~300 Afro-Eurasian populations (~4k individuals) in which we find long-distance migration events from Madagascar and Papuan populations. Coincidentally, we also found that signals of archaic admixture could be captured via the proposed method in simplistic simulations. But before we can celebrate, we need to validate these findings using parallel methods of inquiry. We are also currently in the process of testing this framework with more simulations to make it more robust to spurious signals in the data. 

Poster for Evolution 2023 can be found here <a href="/docs/Evolution_2023.pdf" target="_blank"><i class="fa fa-file-text fa-md"></i></a>. 

### Previous 

#### Estimating genotype and ancestry in hybrids of mixed-ploidy 

(methods development) As part of my MS thesis, I worked on extending a hierarchical Bayesian model presented in [Gompert et al, 2014](https://cpb-us-e1.wpmucdn.com/wp.txstate.edu/dist/a/171/files/2013/05/gompert14.pdf) to run with mixed-ploidy species. The model uses genotype-likelihood data to estimate parameters like genotype and ancestry, similar to the [structure](https://web.stanford.edu/group/pritchardlab/structure.html) software, with application to low-coverage sequencing data. The software is written in C++ with the use of GSL and HDF5 libraries. Using this model, we show that [entropy](https://bitbucket.org/buerklelab/mixedploidy-entropy/src/master/) provides finer resolution in admixture proprotion estimates in a diploid-tetraploid hybrid zone of *Arabadopsis arenosa* in central Europe compared to the current standard. 

#### Quantifying genetic diversity of *Wolbachia* in *Lycaeides* populations

(empirical) *Wolbachia* is an endosymbiotic bacteria that is found in a majority of all insect species and its infection leads to a variety of detrimental phenotypic effects to the population biology of its hosts. However, infection dynamics across species ranges are largely under studied. In this study, we used GBS data from 2388 host butterflies from 109 populations across the United States to quantify the rate and mode of infection in our system using a bioinformatics approach. We find that most of our populations have very high rates of infection (mean = 91%) and that there are three major strains of *Wolbachia* infecting our butterfly species. More information in this [preprint](https://www.authorea.com/doi/full/10.22541/au.164703040.01856976/v1). 

#### Modeling differential abundance testing in microbial count data

(methods development) As part of a lab project to quantify differential abundance in microbial count data, I ported code to model microbial (and ecological) count data to Hamiltonian MC with Stan. This led to faster and more accurate results than the previously used method with Gibbs sampling in JAGS. The model is written into an R package [CNVRG](https://rdrr.io/github/JHarrisonEcoEvo/CNVRG/) that takes as input an OTU table from different treatments (for example, case and control) and fits a Dirichlet-Multinomial conjugate distribution to these two data sets. The ditribution of parameter estimates for the frequencies of the microbes in the two groups are output, after which the question of whether their abundance is different between the two treatments can be answered with a more parametric basis. 
