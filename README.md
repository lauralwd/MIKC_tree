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
![preliminary figure](figures/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1_iqtree-b1000_booster_withrnaseq.svg)

## Guide through files and directories

### Directories

### JuPy notebooks
This repository contains many JuPy notebooks in which we stepwise tried to get a better phylogenetic signal of MIKC evolution and interpretation of the placement of fern sequences.
Here I list very briefly the main conclusion or improvement for each of these files in their chronological order

In `MIKC_tree_workflow-v1.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-v1.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-v1.html)
[iToL](https://itol.embl.de/tree/9421021579373181591777160))
we make a first version of a MIKC tree.
We sample MIKC(-like) genes from specific species across all major groups of plants as described in the 1kP project.

In `MIKC_tree_workflow-v2.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-v2.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-v2.html)
[iToL](https://itol.embl.de/tree/9421021579263431592334615))
we replace some species with others, add bryophytes and lycophytes, and attempt to introduce an outgroup of non-plant sequences.

In `MIKC_tree_workflow-basalclades-v1.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v1.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v1.html)
[iToL](https://itol.embl.de/tree/9421021579288351592221930))
we attempt to improve the phylogenetic signal by sampling less sequences in more recent branches; about a third compared to the previous workflow.

In `MIKC_tree_workflow-basalclades-v2.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v2.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v2.ipynb)
[iToL_gt4](https://itol.embl.de/tree/13121158204159901593010248))
I add _Salivinia cuculata_ sequences from [fernbase](fernbase.org) and remove some sequences that were behaving oddly due too large horizontal gaps in the alignment.
Finally the _Chara globularis_ MADS1 sequence was added, like in the 1kP capstone paper to serve as an outgroup.

In `algal sequences.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/algal%20sequences.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/algal_sequences.html)
)
I extract and align all sequences from the MIKC orthogroup from the 1kP project in an effort to identify those algal sequences which truly have all four domains: M, I, K and C.
We found that in this orthogroup sequences almost always have the highly conserved M domain, but often lack the IKC domains or part thereof.
Based on these results, we proceed only with algal sequences that contain all four domains.

In `MIKC_tree_workflow-basalclades-v3.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v3.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v3.ipynb)
[iToL](https://itol.embl.de/tree/13121159166346421593419936))
I aim to identify non MIKC sequences and remove these from the analyses;
hence I'm making a phylogeny of only MIKC genes and not sequences which only have an M domain.
In a separate notebook, I already did so for all algal sequences in the 1kP MIKC orthogroup.
These should confirm the placing of the CgMADS1 sequence and provide a solid root to the tree.

In `MIKC_tree_workflow-basalclades-v4.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v4.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v4.ipynb)
[iToL](https://itol.embl.de/tree/9421021579173651593446746))
I remove some sequences and run the tree with non-parametric bootstraps instead.

In `MIKC_tree_workflow-basalclades-v5.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v5.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v5.ipynb)
[iToL](https://itol.embl.de/tree/9421021579163171593685733))
I added gymnosperms and _Azolla_ sequences.
Since the algal outgroup has proven to be stable but also very big, it's size is trimmed down.

In `MIKC_tree_workflow-basalclades-v6.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v6.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v6.ipynb)
[iToL-UFbootstrap](https://itol.embl.de/tree/942102157910201593716454))
[iToL-nonparametric](https://itol.embl.de/tree/1312115964226201597403301#))
some _Azolla_ sequences were removed again and a big clade of MIKC* sequences was removed.
MIKC* sequences are characterised by a longer C domain.

In `MIKC_tree_workflow-basalclades-v7.ipynb` 
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v7.ipynb)
html
several rogue taxa were removed; those taxa that were poorly supported and moved around the tree inbetween different inferences.
Also, the algal outgroup was reduced in size and I experimented with different extents of column-content trimming.
I varied the miniumum sequence content per column from 10% to 50% and made UFBootstrap tree inferences:
iToL UFbootstrap 
[gt .1](https://itol.embl.de/tree/131211596429601597651059)
[gt .2](https://itol.embl.de/tree/131211596429631597651059)
[gt .3](https://itol.embl.de/tree/131211596429651597651060)
[gt .4](https://itol.embl.de/tree/131211596429721597651060)
[gt .5](https://itol.embl.de/tree/131211596429741597651061)
Based on the alignments and the trees, I choose the 50% sequence content alignment and made a nonparmetric tree:
itol-nonparametric



## Data sources
1kP

Zhang et al.

more?

## Other links
 * lab page
 * other github pages
 * people involved
 * blank workflow
