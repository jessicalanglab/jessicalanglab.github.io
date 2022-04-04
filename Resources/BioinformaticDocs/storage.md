---
layout: page
title: Storage of data
description: Lab best practices for data storage
background: '/img/bg-about.jpg'
---

<!---
Placeholder for TOC
--->

## Importance of data storage
Sequencing is expensive!! So is time and computing resources!! Be very thoughtful in what and how you remove old data. Tend to err towards saving too much, as we can always remove data later on, but we are less likely to be able to recover it.   
Reproducibility is also essential to both internal and external continuity of the work we do in the lab. Capture in scripts, markdown, or other notes the steps taken to generate the data. Generally, this is extremely small in file size, so it should always be stored.  
Some data storage is more accessible than others, and different data storage types offer different degrees of data security.

## Where to store data?

### Long-term (archival)
Where: (TBD)  
When: ALWAYS  
What: Minimally, .cram formatted files should be saved. This is optimal from a space perspective, as .cram files are smaller than .bam files, and can be converted to .fastq without any loss of data. Maintain inventory of data with description of where it came from (method TBD).

### Near-term
Where: RestrictedDrive (for Lang Lab space, netID is kueck)  
When: Until publication and/or analysis plans completed  
What: All relevant data outputs from sequencing and/or pipelines/analysis (eg. NextFlow output, individually run modules/software output)

OR

Where: Google Drive (Lang Lab space)  
When: Until publication and/or analysis plans completed  
What: Only small files and **no PHI**. Can be handy for easier access to late analysis types (i.e. figures, tables or expression matrixes, etc.)

### Short-term
Where: BRC VM or local storage  
When: When actively working with data  
What: Required input files for tools on BRC VM or local programs, any other active analysis (i.e. R scripts/output/Rmd)

## See also:
[Data transfers on BRC VM](https://jessicalanglab.github.io/Resources/BioinformaticDocs/ComputingPlatforms)  
[RestrictedDrive/ResearchDrive](https://kb.wisc.edu/researchdata/internal/page.php?id=93998)  
[Globus](https://app.globus.org/)
