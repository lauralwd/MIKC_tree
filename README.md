This respository details our work towards placing _Azolla filiculoides_ MIKC genes in a broader picture of MIKC transcription factor evolution.
The phylogeny created here, is featured in [this preprint](https://www.biorxiv.org/content/10.1101/2020.09.09.289736v2).
Many results made publicly available here, are intermediate results and should be treaded as such.
For the final results, please refer to the quick links listed below

manuscript doi: [preprint](https://www.biorxiv.org/content/10.1101/2020.09.09.289736v2)

repository doi: pending

## Quick links
Final input, output and intermediate files:
* [fasta](data/MIKC_orthogroup_selection-basal-v9_guide-v4.fasta)
* alignment [raw](data/alignments_raw/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank.fasta) &
          [trimmed](data/alignments_trimmed/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1.fasta)
* tree in [newick](analyses/MIKC_orthogroup_selection-basal-v9_guide-v4_trees/aligned-mafft-einsi_prank_trim-gt1/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1_iqtree-b1000_booster.treefile)
          ,[png](figures/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1_iqtree-b1000_booster_withrnaseq.png)
          , [pdf](figures/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1_iqtree-b1000_booster_withrnaseq.pdf)
          & [inkscape_svg](figures/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1_iqtree-b1000_booster_withrnaseq.svg)

## Final figure as shown in Dijkhuizen et al. 2021
![](figures/MIKC_orthogroup_selection-basal-v9_guide-v4_aligned-mafft-einsi_prank_trim-gt1_iqtree-b1000_booster_withrnaseq.svg)

## Guide through files and directories

### Directories
The five directories in this respository should be reasonably self explanatory. 
The `data` directory contains input sequences and alignments.
Since I don't consider phylogenetic trees to be data, I store these in the `analyses` directory.
Because jupy notebooks don't always render too well on GitHub, I included several html "print-outs" in the `docs` directory.
For any questions about software versions used: conda environments used in the analyses documented here are available in the `envs` directory.
If no specific conda environment is listed in the notebooks, then the default environment 'phylogenetics' was used.
Finally, the `figures` directory contains two manually "polished" versions of the phylogenetic tree and annotating data for direct inclusion in a journal submission.

### JuPy notebooks
This repository contains many JuPy notebooks in which I and my colleagues stepwise tried to get a better phylogenetic signal of MIKC evolution and interpretation of the placement of fern sequences.
In this itterative process, MIKC protein sequences were aligned, filtered, a tree was infered, and we concluded.
Each notebook describes one itteration of this process. 
Here I list briefly the main conclusion or improvement for each of these notebooks in their chronological order.

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
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v2.html)
[iToL_gt4](https://itol.embl.de/tree/13121158204159901593010248))
I add _Salivinia cuculata_ [sequences](data/salvinia_sequences/salivinia_fernbase_blast_results_uniq.fasta) from [fernbase](https://www.fernbase.org) and remove some sequences that were behaving oddly due too large horizontal gaps in the alignment.
Finally the _Chara globularis_ MADS1 sequence was added, like in the [1kP capstone paper](https://doi.org/10.1038/s41586-019-1693-2) to serve as an outgroup.

In `algal sequences.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/algal_sequences.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/algal_sequences.html)
)
I extract and align all algal sequences from the MIKC orthogroup from the 1kP project in an effort to identify those algal sequences which truly have all four domains: M, I, K and C.
We found that in this orthogroup sequences almost always have the highly conserved M domain, but often lack the IKC domains or part thereof.
Based on these results, we proceed only with algal sequences that contain all four domains.

In `MIKC_tree_workflow-basalclades-v3.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v3.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v3.html)
[iToL](https://itol.embl.de/tree/13121159166346421593419936))
I aim to identify non MIKC sequences and remove these from the analyses;
hence I'm making a phylogeny of only MIKC genes and not sequences which only have an M domain.
In a separate notebook, I already did so for all algal sequences in the 1kP MIKC orthogroup.
These should confirm the placing of the CgMADS1 sequence and provide a solid root to the tree.

In `MIKC_tree_workflow-basalclades-v4.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v4.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v4.html)
[iToL](https://itol.embl.de/tree/9421021579173651593446746))
I remove some sequences and run the tree with non-parametric bootstraps instead.

In `MIKC_tree_workflow-basalclades-v5.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v5.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v5.html)
[iToL](https://itol.embl.de/tree/9421021579163171593685733))
I added gymnosperms and _Azolla_ sequences.
Since the algal outgroup has proven to be stable but also very big, it's size is trimmed down.

In `MIKC_tree_workflow-basalclades-v6.ipynb`
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v6.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v6.html)
[iToL-UFbootstrap](https://itol.embl.de/tree/942102157910201593716454)
[iToL-nonparametric](https://itol.embl.de/tree/1312115964226201597403301#))
some redundant _Azolla_ sequences were removed again and a big clade of MIKC* sequences was removed.
MIKC* sequences are characterised by a longer C domain.

In `MIKC_tree_workflow-basalclades-v7.ipynb` 
([ipynb](https://github.com/lauralwd/MIKC_tree/blob/master/MIKC_tree_workflow-basalclades-v7.ipynb)
[html](https://htmlpreview.github.io/?https://github.com/lauralwd/MIKC_tree/blob/master/docs/MIKC_tree_workflow-basalclades-v7.html))
several rogue taxa were removed; those taxa that were poorly supported and moved around the tree inbetween different inferences.
Also, the algal outgroup was reduced in size and I experimented with different extents of column-content trimming.
I varied the miniumum sequence content per column from 10% to 50% and made UFBootstrap tree inferences:
iToL UFbootstrap 
[gt .1](https://itol.embl.de/tree/131211596429601597651059)
[gt .2](https://itol.embl.de/tree/131211596429631597651059)
[gt .3](https://itol.embl.de/tree/131211596429651597651060)
[gt .4](https://itol.embl.de/tree/131211596429721597651060)
[gt .5](https://itol.embl.de/tree/131211596429741597651061)
Based on the alignments and the trees, I choose the 50% sequence content alignment and made a non-parametric tree only to find that bootstrap support broke down completely:
[itol-nonparametric](https://itol.embl.de/tree/1312115999190001598359608).



## Data sources
1kP

Zhang et al.

more?

## Other links
 * lab page
 * other github pages
 * people involved
 * blank workflow
