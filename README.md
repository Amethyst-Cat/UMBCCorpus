# UMBCCorpus
A project analyzing sensory descriptors from the [UMBC Corpus](https://ebiquity.umbc.edu/blogger/2013/05/01/umbc-webbase-corpus-of-3b-english-words/).

## UMBC_analysis Python Notebook
All code used to analyze the corpus is [here](https://github.com/Amethyst-Cat/UMBCCorpus/blob/master/UMBC_analysis.ipynb).

Sections "Fix UMBC Corpus", "Train Word2Vec Model", "Identify Contexts", and "Calculate OAI from CSV" are code taken directly from the project [Mapping the semantic organization of odor vocabulary using natural language data](https://osf.io/zpm5y/). 

Sections "NMF" and "PCA" conduct non-negative matrix factorization and principal component analysis on the pearson distance matrix of the word embeddings for specific descriptors.
Section "Clustering" generates dendrograms from Pearson distance matrices.
Sections "Intersect DataFrames" and "Set Difference" perform intersection and differences on descriptor tables.
Section "Open JSON Sentence Files" searches JSON sentence files for sentences matching search words.
Sections "POS Frequencies", "Intersection with Modality", "Intersection with Concreteness" generate corresponding statistics from descriptor tables.
Section "Heatmap" generates the heatmap graph.

## Top 300 Descriptor OAI Files
The [folder "descriptors"](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/descriptors) contains the top 300 descriptors by OAI for all perception verbs, as well as the Lancaster and Concreteness descriptor data.

## Dendrograms
All dendrograms created using hierarchical clustering are located in the [dendrograms folder](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/dendrograms).

## Descriptor Intersections
Tables containing all descriptors in the intersection of two perception verbs are located in the [intersections folder](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/intersections). Additionally, data of the number of descriptors in each intersection is in the file "DescriptorDataTables.xlsx".

## Lancaster Descriptor Data
Lancaster data for perception descriptors are located in the [Lancaster folder inside the intersections folder](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/intersections/Lancaster).

## Modality Intersection Data
Information about the descriptors per modality, the POS distribution, and count for each perception verb are located in the [statistics folder](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/statistics).

## Exclusivity and Strength Scores
Exclusivity and Strength scores for each descriptor are located in the [modaility_intersection_strength folder inside the statistics folder](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/statistics/modality_intersection_strength).

## POS Distribution Charts, Histograms, Heatmaps
Located in the [statistics folder](https://github.com/Amethyst-Cat/UMBCCorpus/tree/master/statistics).

## PCA, NMF 
Graphs labelled PC1 to PC3 first_40_desciptors and last_40_descriptors contain the 40 descriptors on both ends for each principal component and their principal component values. Principal components were determined by running PCA on the distance matrix for the 300 feel descriptors filtered by OAI. PC1 explains 24% of the variance, PC2 explains 18%, PC3 explains 13%. 

10_15_components contains the results of NMF run on the 300-descriptor distance matrix. Each component and its 15 most relevant words are identified, along with their weights.
NMF_Feel_Descriptors contains the results of NMF run on the 300-descriptor distance matrix and the 200-descriptor purple cluster words. Each component and its most relevant words are identified, along with their weights.
