---
layout: default
title: sample proposal
---


## Contact Information

Yosemite Sam, professor of Genome Sciences, PoDunk State University.

## Project Summary:

The goal of the study is to assemble a variety of genome-wide data sets and use
them to train a discriminative classifier. The labels for the task correspond to
two sets of genomic coordinates, one consisting of 15 million SNPs that have
become fixed in the human population since the human/chimp divergence, and one
consisting of 15 million randomly generated SNPs (Single-nucleotide
polymorphism). The features for the task consist of a variety of different types
of data, including several different base-level phylogenetic conservation
scores, a curated gene annotation indicating the locations of protein-coding
regions, as well as a collection of experimental data sets. The total set of
features is roughly 65. 

## About the Data :

Much of the data is publicly available in the UCSC Genome Browser Database
(GBD). Information based on gene models (i.e. distance to exon/intron
boundaries, resulting amino acid alteration, etc.) as well as SIFT/PolyPhen
scores are obtained through Ensembl Variant Effect Predictor (VEP).  

The complete set of feature vectors for all 9 billion possible SNPs are stored
in a directory containing thousands of smaller files, comprising ~1TB of disk
space. Also stored are the subsets of 30M positive and negative labeled sets, as
well as a 10-fold random split of those data. 

All of our data is stored on a network file system that is maintained by the
Genome Sciences department. 

## Challenges:

We face several data analysis challenges.  First, many of the feature sets
contain missing values. These missing values must be imputed, and then
additional boolean features added to indicate missingness. Second, each
categorical feature must be expanded into a collection of binary features. This
increased the size of the feature set to several hundred. Third, because of the
large size of the training set, the authors plan to apply a linear
classification model. Therefore, to incorporate their prior knowledge about
which pairs of features are likely to exhibit informative correlations, several
hundred feature-pairs must be identified and added to the initial feature
set. This increases the feature set even further, to approximately 1000. 

The size of the resulting data sets makes the use of simple scripts prohibitive.
We are struggling to find techniques that operate at this scale, yet are simple
to learn, use, and extend. 

## Timeline:

Our ambitious goal is to submit a paper to Nature in the Fall of 2014.  We would
also like to prepare a workshop paper in late spring of 2014, but this can be
based on more tentative results. 

## Who will collaborate:

Wile E. Coyote, a graduate student in genome science, will be the primary point
of contact.  He is willing to sit in the incubator space on monday and wednesday
afternoons. 