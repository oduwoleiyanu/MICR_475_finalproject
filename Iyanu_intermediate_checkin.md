Intermediate checkin
================

**Class project title: Quantifying the Genomic novelty and Taxonomic
distance between Archaea MAGs and Isolates**

Sequence similarity searching using NCBI tools such as BLAST is one way
to determine and quantify the identities of microbes by comparing their
sequences to their closest culture relatives(Lloyd et al., 2018). This
search reports a similarity score (Bitscore) where the increase in
Bitscore indicates increase in sequence similarity(Pearson, 2013;
Weisman et al., 2020). Homologs descend from common evolutionary
ancestry, and homologs detected only within a taxa level such as
species, are referred to as novel or taxonomy restricted genes(Weisman
et al., 2020). My prediction is that homologs detected through the
similarity scores approach in Archaea MAGs may have some relationship to
the taxonomic distance between the MAGs and isolates and basically how
much these similarity scores explains cultured level the MAGs belongs
to. I would also look at how the homologs of these subgroups are
distributed at the individual levels. I would demonstrate this by
exploring this data using different visualization tools and regression
models. I would also look at the possibility of using statistical tests
to see if the two models are different

Work flow

Work flow a) load the Archaea MAGs (GEM metadata file containing the
taxonomy and environment information) b) load the Archaea taxonomy file
downloaded from the GTDB which would serve as the isolate taxonomy
database c) Split the two datasets into separate distinct columns c)
load the Archae_diamond dataset which contain the similarity scores
information such as the Bitscores, e-values, percentage identity,
Alignment length, query lengths and others. d) Filter for only the
Refseq in Archea taxonomy file e) Using the function unique, make a
vector of each taxa level from the Refseq archaea file f) Filter for
Archaea MAGs of each taxa level that matches the unique taxa level of
the RefSeq and create(mutate) two new columns (taxonomic distance and
cultured level) g) Merge this data with the Archaea_diamond dataset
(similarity_score dataset) h) Apply several filtering thresholds to the
query length and bit scores i) create a new column with a normalized bit
score (bit scores/alignment length). j) Generate 1000 sample size k)
Make a normalized bit score and taxonomic distance regression model
using ggplot exploiting different filtering thresholds.  
l) Repeat the same plot for the percentage identity instead of
normalized bitscore m) Create a boxplot of normalized bit score and
cultured level n) Split the taxa at the phyla level, make a group of the
highly cultivated and less cultivated groups, and visualize using a box
plot. o) Analyze any statistically significant difference among the taxa
levels using ANOVA.
