Scenario
=====

Protozoan blood parasites undergo radical changes in terms of gene and protein expression during their life cycle phases in host and vector. 
We will use a Plasmodium falciparum RNAseq dataset to investigate which genes play specific roles during the stay of the parasite in the host. 

Starting with the raw RNAseq dataset, we will identify changes in expression between different life cycle stages and then integrate this information with P. falciparum interactome networks, to locate region of the interactome that might represent functional modules involved in this  process. 

Dataset
=====

A starting point for the project will be the raw data from: 

BMC Genomics. 2011 Nov 30;12:587. doi: 10.1186/1471-2164-12-587. http://www.ncbi.nlm.nih.gov/pubmed/22129310
López-Barragán MJ, Lemieux J, Quiñones M, Williamson KC, Molina-Cruz A, Cui K, Barillas-Mury C, Zhao K, Su XZ
Directional gene expression and antisense transcripts in sexual and asexual stages of Plasmodium falciparum. 

We will take also advantage of the available data in PlasmoDB http://plasmodb.org/plasmo/

Project aims:

+ Process raw RNA seq data
  + Integrate RNAseq information with the interactome
  + Quality check of the reads + Filtering 
  + Mapping to the genome
  + Quantification of expression levels
  + Differential expression analysis
  + Import protein interaction information using Cytoscape
  + Confidence score fitering

+ Integrate differential expression values in your network
  + ID mapping
  + Expression values visualization
  + Functional analysis of the network
  + Topology analysis
  + Annotation enrichment analysis
