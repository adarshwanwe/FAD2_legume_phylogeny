# Comparative Evolutionary Analysis of FAD2 Proteins in Legume Crops

> A comparative bioinformatics study investigating the evolutionary conservation and phylogenetic relationships of Fatty Acid Desaturase 2 (FAD2) proteins across key legume species.

---

## Table of Contents

- [Background](#background)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Project Workflow](#project-workflow)
- [Repository Structure](#repository-structure)
- [Tools & Software](#tools--software)
- [Conclusion](#conclusion)

---

## Background

Fatty Acid Desaturase 2 (FAD2) is a key enzyme responsible for the conversion of oleic acid (C18:1) to linoleic acid (C18:2), a reaction central to polyunsaturated fatty acid biosynthesis. FAD2 activity directly influences oil composition and quality in legumes and oilseed crops, making it a gene of significant agricultural and nutritional importance.

This project applies comparative bioinformatics approaches — sequence alignment, BLAST homology search, and phylogenetic reconstruction — to investigate how FAD2 proteins have been conserved and diverged across major legume species.

---

## Objectives

- Retrieve FAD2 homolog sequences from representative legume species using NCBI BLASTP
- Assess pairwise and multiple sequence similarity among FAD2 proteins
- Perform multiple sequence alignment (MSA) using Clustal Omega
- Construct a Neighbor-Joining phylogenetic tree with bootstrap validation
- Interpret conservation patterns and evolutionary relationships of FAD2 across legumes

---

## Dataset

### Query Sequence

| Field | Detail |
|---|---|
| Species | *Glycine max* (Soybean) |
| Accession | `NP_001341865.1` |
| Protein | Omega-6 Fatty Acid Desaturase (FAD2) |

### Homologous Sequences Retrieved via BLASTP

| Species | Common Name | Accession |
|---|---|---|
| *Glycine soja* | Wild soybean | `KAL5194686.1` |
| *Cajanus cajan* | Pigeonpea | `XP_082916432.1` |
| *Vigna unguiculata* | Cowpea | `XP_027935617.1` |
| *Phaseolus vulgaris* | Common bean | `KAL9317095.1` |
| *Vigna radiata* | Mung bean | `XP_014511999.1` |
| *Arachis hypogaea* | Peanut | `AAY67653.1` |
| *Lotus japonicus* | Lotus | `XP_057424649.1` |
| *Cicer arietinum* | Chickpea | `XP_004497140.1` |

---

## Methodology

1. **Query Sequence** — Soybean FAD2 protein (`NP_001341865.1`) retrieved from the NCBI Protein database.
2. **Homolog Identification** — NCBI BLASTP used to identify homologous FAD2 sequences across legume species.
3. **Sequence Retrieval** — Target protein sequences downloaded from NCBI in FASTA format.
4. **Multiple Sequence Alignment (MSA)** — Clustal Omega used to align all sequences (`FAD2_sequences.fasta`).
5. **Format Conversion** — Alignment files converted to MEGA-compatible format using EMBOSS Seqret.
6. **Phylogenetic Tree Construction** — Neighbor-Joining (NJ) tree built in MEGA.
7. **Bootstrap Validation** — Statistical support assessed with 1000 bootstrap replications.

---

## Results

### BLAST Analysis

All selected homologs showed **100% query coverage** and high sequence identity with the *Glycine max* FAD2 protein, confirming strong conservation of this enzyme across the legume family.

![BLAST Results]
(blast_results.png)

### Multiple Sequence Alignment

The MSA revealed a high degree of sequence conservation across all studied legume FAD2 proteins, consistent with strong purifying selection on a functionally essential enzyme.

![Clustal Omega Alignment]
(clustal_alignment.png)

### Phylogenetic Analysis

The Neighbor-Joining tree grouped species in accordance with established legume taxonomy.

![Phylogenetic Tree]
(phylogenetic_tree.png)

Key observations:

- ***Glycine max* and *Glycine soja*** formed a strongly supported sister clade (Bootstrap = **100**), reflecting their close taxonomic relationship.
- ***Vigna radiata* and *Vigna unguiculata*** clustered together with strong bootstrap support (Bootstrap = **96**).
- ***Phaseolus vulgaris*** grouped close to the *Vigna* lineage, consistent with their shared membership in the tribe Phaseoleae.
- FAD2 proteins showed **high overall conservation** across all studied legumes, reinforcing the functional importance of this enzyme in fatty acid metabolism.

---

## Project Workflow

```
Soybean FAD2 Protein (NP_001341865.1)
        │
        ▼
  NCBI BLASTP Search
        │
        ▼
  Homolog Retrieval (8 species)
        │
        ▼
  Multiple Sequence Alignment
     (Clustal Omega)
        │
        ▼
  Format Conversion
    (EMBOSS Seqret)
        │
        ▼
  Phylogenetic Analysis (MEGA)
  Neighbor-Joining + 1000 Bootstrap
        │
        ▼
  Evolutionary Interpretation
```

---

## Repository Structure

```
FAD2-Legume-Evolution/
├── FAD2_sequences.fasta       # Unaligned FASTA sequences (query + homologs)
├── Aligned_sequences.fasta    # Clustal Omega multiple sequence alignment output
├── blast_results.png          # BLASTP results screenshot
├── clustal_alignment.png      # MSA visualization
├── phylogenetic_tree.png      # Neighbor-Joining phylogenetic tree
└── README.md
```

---

## Tools & Software

| Tool | Purpose | Link |
|---|---|---|
| NCBI Protein Database | Sequence retrieval | [ncbi.nlm.nih.gov](https://www.ncbi.nlm.nih.gov/protein/) |
| NCBI BLASTP | Homolog identification | [blast.ncbi.nlm.nih.gov](https://blast.ncbi.nlm.nih.gov/) |
| Clustal Omega | Multiple sequence alignment | [ebi.ac.uk/Tools/msa/clustalo](https://www.ebi.ac.uk/Tools/msa/clustalo/) |
| EMBOSS Seqret | Alignment format conversion | [ebi.ac.uk/Tools/sfc/emboss_seqret](https://www.ebi.ac.uk/Tools/sfc/emboss_seqret/) |
| MEGA | Phylogenetic tree construction | [megasoftware.net](https://www.megasoftware.net/) |

---

## Conclusion

This study demonstrates strong evolutionary conservation of FAD2 proteins across legume crops. Phylogenetic analysis confirmed close relationships among taxonomically related species and validated the Neighbor-Joining approach for resolving intra-family divergence. The results highlight the utility of comparative bioinformatics for studying functionally important genes involved in fatty acid metabolism and oil quality — with potential implications for crop improvement programs targeting seed oil composition.

---

*Study conducted using publicly available sequence data from NCBI. All tools used are freely accessible online.*
