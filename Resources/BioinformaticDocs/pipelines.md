---
layout: page
title: Lang Lab Pipelines
description: Standardized workflows for genomics analysis
background: '/img/bg-about.jpg'
---

#### Bioinformatics Docs Table of Contents
+ [GitHub](https://jessicalanglab.github.io/Resources/BioinformaticDocs/GitHub)
+ [Computing platforms](https://jessicalanglab.github.io/Resources/BioinformaticDocs/ComputingPlatforms)
+ [Lab Pipelines](https://jessicalanglab.github.io/Resources/BioinformaticDocs/pipelines)
+ [Data Storage](https://jessicalanglab.github.io/Resources/BioinformaticDocs/storage)
+ [Electronic Lab Notebooks for Bioinformatics](https://jessicalanglab.github.io/Resources/BioinformaticDocs/notes)

## Genomics analysis pipelines
Our lab is using NextFlow, a workflow manager for scientific analysis, primarily focused on genomic analysis. The nextflow core (nf-core) community has developed well-tested workflows for many standard analyses that we will leverage directly. These are implemented from docker images that pull in all necessary software, etc. to run the pipeline. Read more in the [Nextflow](https://www.nextflow.io/docs/latest/index.html) and [nf-core](https://nf-co.re/) documentation.

### NextFlow pipelines of note
| Pipeline name | Use |
| --- | --- |
| nf-core/rnaseq | RNA-seq |
| nf-core/cutandrun | CUT&RUN |
| nf-core/sarek | WES/WGS variant calling |
| nf-core/fetchngs | fetch public/private NGS |
| nf-core/hic | Hi-C |
| nf-core/methylseq | DNA methylation seq |
| nf-core/chipseq | ChIP-seq |
| nf-core/scrnaseq | single-cell RNA-seq |
| nf-core/atacseq | ATAC-seq |

### Using NextFlow within our BRC VM
NextFlow is not available as official BRC software, but we have installed it in our home directory. To run NextFlow commands:
> cd /home/BIOTECH/jlang/tools/nf
> ./nextflow <your command, inputs and arguments as required by nextflow>

Try a test NextFlow run to make sure everything is working as expected. We use the Singularity profile, since Singularity is installed on BRC. Below is an example for the RNA-seq pipeline, but you can see each tool's documentation for how to run a test.
> ./nextflow run nf-core/rnaseq -profile test,singularity --outdir /home/BIOTECH/jlang/results/RNAseq/<foldername>

To run your own data, generally you need to check the following things:
+ Availability of data you want to analyze within the BRC VM
+ Input in proper format for that pipeline (see individual nf-core tool documentation)
+ Output directory specified where you can find the results. We typically place this all in the /home/BIOTECH/jlang/results folder, but please make sure to create a subdirectory with a descriptive name and **your initials** so we know who owns the data (since we are using a shared login)

Final results should be transferred back to ResearchDrive for storage, and removed from the BRC VM when you are done actively using it. Until the data is published, all NextFlow output should be retained.

### Connecting to NextFlow community
You may find it helpful to join the [nf-core community](https://nf-co.re/join) on Slack or GitHub if you become a frequent user and need to modify the pipelines or report issues.
