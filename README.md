# Lineage designations for RSV-B

## **2025-07-01**: Upcoming automated download for the review of emerging lineages, based on genome sequences available as of that date from the International Nucleotide Sequence Database Collaboration (NCBI GenBank, EBI, and DDBJ) and the Pathoplexus databases.

This repository contains the definitions of lineages for RSV-B following the proposal put forward in  [**Standardized Phylogenetic Classification of Human Respiratory Syncytial Virus Below the Subgroup Level**](https://wwwnc.cdc.gov/eid/article/30/8/24-0209_article) by Goya et al and the RSV Genotyping Consensus Consortium.

Please refer to the preprint for an in-depth discussion of the lineages and nomenclature. You can assign your own sequence data to the different lineages using [Nextclade](https://clades.nextstrain.org) or [UShER](https://genome.ucsc.edu/cgi-bin/hgPhyloPlace).

## [Summary of designated lineages](.auto-generated/clades.md)


## Lineage maintenance

To define a new lineage, add "lineage YAML" file to the folder `lineages`. These files have the following format
```yaml
defining_mutations:
  - locus: F
    position: 172
    state: Q
  - locus: F
    position: 103
    state: V
name: B.D.4
parent: B.D
representatives:
- OK649704
- OK649708
- OK649705
- OK649728
- OK649726
- KY249677
- KY249670
- KY249667
unaliased_name: B.5.4
```

Once a new yaml file got added and merged into master, run the [helper scripts](https://github.com/rsv-lineages/helper-scripts) to regenerate the autogenerated markdown summaries and clade-tsv files.
```shell
python ../helper-scripts/generate_markdown_summary.py --input-dir lineages --lineage B
python ../helper-scripts/construct_tsv.py --input-dir lineages --output-tsv .auto-generated/lineages.tsv
```
