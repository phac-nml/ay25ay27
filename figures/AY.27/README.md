# Analysis of AY.27

This repository contains the code for the analysis of AY.27 to produce a phylogenetic tree alongside a heatmap of mutations using data from GISAID.

The final figure is found in [2-mutation-ay27.ipynb][]

# 1. Copy data

```bash
cp ../../twentysevenext/*.nwk .

# Replace this line to copy/link all GISAID sequences
ln -s /Drives/P/Auspice/ncov/data/gisaid_sequences.fasta input/

# Replace these lines to copy/link to GISAID metadata (subsampled to only those found in the tree)
cp /Drives/K/apetkau/workspace/nml-ay25-ay27-2021-11-05/twentysevenext-2021-11-08/twentysevenext_subsampled_metadata.tsv.xz input/
xz -d input/twentysevenext_subsampled_metadata.tsv.xz
gzip input/twentysevenext_subsampled_metadata.tsv
```

# 2. Extract sequences/prepare input

Run the following notebooks:

```
conda activate gdi-nml-ay27
```

* [1-extract-sequences.ipynb][]

# 3. Build index

Run the following:

```bash
gdi init index

gdi --project-dir index/ --ncores 32 analysis --reference-file ../references/NC_045512.gbk.gz --input-structured-genomes-file input/gdi-input-gisaid.tsv
```

# 4. Create figure

Run the following notebook:

* [2-mutation-ay27.ipynb][]
