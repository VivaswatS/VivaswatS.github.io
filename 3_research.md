---
layout: page
title: "Research"
description: "evolutionary and population genetics"
header-img: "img/brycecanyon.jpg"
---

### Ongoing

#### Quantifying genetic diversity of *Wolbachia* in *Lycaeides* populations

*Wolbachia* is an endosymbiotic bacteria that is maternally transmitted in its hosts. Here, we used GBS data from 2388 butterfly individuals from 109 populations across the United States to answer three main questions:  
1. Can we detect *Wolbachia* infection from host genomes *in-silico* through bioinformatic approches?  
2. What is the extent to which the bacteria has integrated into the nuclear genome of its host i.e., how big are the NUMTs?  
3. Are the patterns in genetic diversity of *Wolbachia* expected based on the genetics of the host? If not, how are they different?  
With these in mind, we set out to run the analysis using traditional population genetics approaches with modifications to accommodate for the nature of this bacteria. 

### Previous 

#### Estimating genotype and ancestry in hybrids of mixed-ploidy 

As part of my MS thesis, I worked on extending a hierarchical Bayesian model presented in [Gompert et al, 2014](https://cpb-us-e1.wpmucdn.com/wp.txstate.edu/dist/a/171/files/2013/05/gompert14.pdf) to run with polyploid species. The model uses genotype-likelihood data to estimates parameters like genotype and ancestry, similar to the [Structure](https://web.stanford.edu/group/pritchardlab/structure.html) software, with application to low- to medium-coverage sequencing data. The software is written in C++ with the use of GSL libraries for random sampling and HDF5 for efficient storage. Using this model, we were able to better estimate ancestry in a mixed-ploidy hybrid zone of *Arabadopsis arenosa* in Europe. 

#### Modeling differential abundance testing in microbial count data

As part of a lab project to quantify differential abundance in microbial count data, I ported the data generative model to use Hamiltonian MC with Stan. This led to faster and more accurate results than the previously used method with Gibbs sampling in JAGS. The model is written into an R package [CNVRG](https://rdrr.io/github/JHarrisonEcoEvo/CNVRG/) that takes as input an OTU table from different treatments (for example, case and control) and fits a Dirichlet-Multinomial conjugate distribution to these two data sets. The ditribution of parameter estimates for the frequencies of the microbes in the two groups are output, after which the question of whether their abundance is different between the two treatments can be answered with a more statistical basis. We show that it outperforms other commonly used methods used in the analysis of microbial and ecological count data. 
