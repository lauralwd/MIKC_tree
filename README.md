This respository details our work towards placing _Azolla filiculoides_ MIKC genes in a broader picture of MIKC transcription factor evolution.
The phylogeny created here, is featured in \[publication\].
Many results made publicly available here, are intermediate results and should be treaded as such.
For the final results, please refer to the quick links listed below

manuscript doi:
repository doi:

## Quick links
Final input, output and intermediate files:
* fasta
* alignment raw & trimmed
* tree in newick, png, pdf & inkscape_svg
* JuPyter notebook detailing all code

## Final figure
\[insert figure\]

## Guide through files and directories

### directories

### JuPy notebooks
This repository contains many JuPy notebooks in which we stepwise tried to get a better phylogenetic signal of MIKC evolution and interpretation of the placement of fern sequences.
Here I list very briefly the main conclusion or improvement for each of these files in their chronological order

In `MIKC_tree_workflow-v1.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-v1.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-v1.html)
)
we make a first version of a MIKC tree.
We sample MIKC(-like) genes from specific species across all major groups of plants as described in the 1kP project.

In `MIKC_tree_workflow-v2.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-v2.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-v2.html)
)
we replace some species with others, add bryophytes and lycophytes, and attempt to introduce an outgroup of non-plant sequences.

In `MIKC_tree_workflow-basalclades-v1.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v1.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v1.html)
)
we attempt to improve the phylogenetic signal by sampling less sequences in more recent branches; about a third compared to the previous workflow.

In `algal sequences.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/algal%20sequences.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/algal_sequences.html)
) I extract and align all sequences from the MIKC orthogroup from the 1kP project in an effort to identify those algal sequences which truely have all four domains: M, I, K and C.
We found that in this orthogroup sequences almost always have the highly conserved M domain, but often lack the IKC domains or part thereoff.
Based on these results, we proceed only with algal sequences that contain all four domains.

MIKC_tree_workflow-basalclades-v2.ipynb
MIKC_tree_workflow-basalclades-v3.ipynb
MIKC_tree_workflow-basalclades-v4.ipynb
MIKC_tree_workflow-basalclades-v5.ipynb
MIKC_tree_workflow-basalclades-v6.ipynb






## Data sources
1kP
Zhang et al.
more?

## Other links
lab page
other github pages
people involved
blank workflow
