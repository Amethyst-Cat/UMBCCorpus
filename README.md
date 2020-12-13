# UMBCCorpus
A project analyzing sensory descriptors from the [UMBC Corpus](https://ebiquity.umbc.edu/blogger/2013/05/01/umbc-webbase-corpus-of-3b-english-words/).

## UMBC_analysis Python Notebook
Sections "Fix UMBC Corpus", "Train Word2Vec Model", "Identify Contexts", and "Calculate OAI from CSV" are code taken directly from the project [Mapping the semantic organization of odor vocabulary using natural language data](https://osf.io/zpm5y/). 

Sections "NMF" and "PCA" conduct non-negative matrix factorization and principal component analysis on the pearson distance matrix of the word embeddings for specific descriptors.

## CSV Files
Descriptor_file_OlfactoryFrequencies contains the frequencies of descriptors in the +/- 4 word context window of the word feel throughout the entire UMBC corpus. Descriptor_file_feel_oai contains frequencies and OAI/OSI scores for a subset of most frequent descriptors on a randomly selected subset of 50 UMBC files to save computation. The descriptors manually identified to be relevant had an OAI of greater than -7.

## PCA Visualizations 
Graphs labelled PC1 to PC3 first_40_desciptors and last_40_descriptors contain the 40 descriptors on both ends for each principal component and their principal component values. Principal components were determined by running PCA on the distance matrix for the 300 feel descriptors filtered by OAI. PC1 explains 24% of the variance, PC2 explains 18%, PC3 explains 13%. 

## Hierarchical Clustering Dendrograms 
dendrogram_feel_descriptors contains the dendrogram from running hierarchical clustering on the distance matrix. purple_feel_descriptors contains the dendrogram created when running hierachical clustering on the roughly 200 words labelled in the purple cluster in original dendrogram. 

## NMF Word Files
10_15_components contains the results of NMF run on the 300-descriptor distance matrix. Each component and its 15 most relevant words are identified, along with their weights.
NMF_Feel_Descriptors contains the results of NMF run on the 300-descriptor distance matrix and the 200-descriptor purple cluster words. Each component and its most relevant words are identified, along with their weights.
