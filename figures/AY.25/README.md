# Analysis of AY.25

This describes the analysis for constructing an AY.25 tree with a mutation heatmap. The analysis started from an Augur analysis directory containing a phylogenetic tree and metadata from GISAID.

The final figure was constructed in this notebook [2-mutation-ay25.ipynb](2-mutation-ay25.ipynb).

# 1. Copy data

```bash
cp ../../twentysevenext/*.nwk .

# Replace this line to copy/link all GISAID sequences
ln -s /path/to/gisaid_sequences.fasta input/

# Replace these lines to copy/link to GISAID metadata (subsampled to only those found in the tree)
cp ../../twentyfiveext/twentyfiveext_subsampled_metadata.tsv.xz input/
xz -d input/twentyfiveext_subsampled_metadata.tsv.xz
gzip input/twentyfiveext_subsampled_metadata.tsv
```

# 2. Extract sequences/prepare input

Run the following notebooks:

```
conda activate gdi-nml-ay27
```

* [1-extract-sequences.ipynb](1-extract-sequences.ipynb)

# 3. Build index

Run the following:

```bash
gdi init index

gdi --project-dir index/ --ncores 32 analysis --reference-file ../references/NC_045512.gbk.gz --input-structured-genomes-file input/gdi-input-gisaid.tsv
```

# 4. Create figure

Run the following notebook:

* [2-mutation-ay25.ipynb](2-mutation-ay25.ipynb)
