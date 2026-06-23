# rnaseq_project2
An educational project completed during the university course "Analysis methods of structural and functional chromatin organization"

This repository contains the scripts and notes for a transcriptomics practice focused on aligning RNA-seq and CAGE-seq reads, generating BAM and coverage tracks, and visualizing them in IGV.

## Overview

The workflow includes:
- STAR alignment of RNA-seq paired-end reads.
- STAR alignment of CAGE-seq single-end reads.
- Optional BWA alignment of RNA-seq reads for comparison.
- BAM indexing and MAPQ >= 30 filtering.
- Coverage track generation as bedGraph and bigWig.

## Tools
- STAR
- BWA
- samtools
- bedtools
- ucsc-bedgraphtobigwig
- FastQC
- MultiQC

## Usage

Download reads:
```bash
python3 scripts/download_raw_reads.py --sample MoPh7
```

Run the full pipeline:
```bash
bash scripts/run_all_star_tracks.sh
```

## Outputs

The pipeline generates:
- sorted BAM files.
- MAPQ 30 BAM files.
- sorted bedGraph files.
- bigWig files for IGV.

Large data files and generated tracks are intentionally excluded from version control.
