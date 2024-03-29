# AY25AY27 additional data

Builds and sample lists from comparison of Canadian AY.25 and AY.27 sequences to global for analysis in <https://virological.org/t/monitoring-the-evolution-and-spread-of-delta-sublineages-ay-25-and-ay-27-in-canada/767>.

# Trees

The trees used to build the figures are:

* **Figure 4**: [AY.25 tree (newick)](twentyfiveext/tree.nwk)
* **Figure 5**: [AY.27 tree (newick)](twentysevenext/tree.nwk)

These trees were built using Augur and the Augur build file is found at [builds.yaml](builds.yaml). Lists of the samples used are found in [twentyfiveext](twentyfiveext) and [twentysevenext](twentysevenext).

# Figures

The figures for AY.25 and AY.25 are found in the following notebooks:

* **Figure 4**: [AY.25 notebook](figures/AY.25/2-mutation-ay25.ipynb)
    * [Other instructions](figures/AY.25)
* **Figure 5**: [AY.27 notebook](figures/AY.27/2-mutation-ay27.ipynb)
    * [Other instructions](figures/AY.27)

To run the analyses for Figures 4 and 5 you will need to install <https://github.com/apetkau/genomics-data-index> and [Jupyter](https://jupyter.org/) and also aquire the set of sequence data/metadata from GISAID (these are not provided).
