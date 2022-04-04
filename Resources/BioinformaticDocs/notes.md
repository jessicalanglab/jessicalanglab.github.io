---
layout: page
title: Electronic Lab Notebooks for Bioinformatics
description: Lab best practices for notes
background: '/img/bg-about.jpg'
---

#### [Bioinformatics Docs](https://jessicalanglab.github.io/Resources/BioinformaticDocs) Table of Contents
+ [GitHub](https://jessicalanglab.github.io/Resources/BioinformaticDocs/GitHub)
+ [Computing platforms](https://jessicalanglab.github.io/Resources/BioinformaticDocs/ComputingPlatforms)
+ [Lab Pipelines](https://jessicalanglab.github.io/Resources/BioinformaticDocs/pipelines)
+ [Data Storage](https://jessicalanglab.github.io/Resources/BioinformaticDocs/storage)
+ [Electronic Lab Notebooks for Bioinformatics](https://jessicalanglab.github.io/Resources/BioinformaticDocs/notes)

## Electronic Lab Notebooks
Electronic Lab Notebooks (ELN) are a documentation of the steps and procedures performed to generate data in the lab. This is essential for lab records, importantly for being able to report data processing in publications and for the lab to replicate data analysis.  
While the wet lab has implemented ELN on the Google Drive, what works for wet lab documentation is a bit different from computational work. In general, our lab supports flexibility in ELN format to maximize the applicability to diverse projects and personal note-taking habits. **The important thing is to be as thorough in documenting your work as you can**. While it can be time consuming, you will almost never regret more information.

## Lang Lab recommendations for documenting bioinformatic work
### Google Drive
Since our lab is part-wet part-bioinformatics, it is handy to have one primary place to look for information. For this reason, Google Drive lab notebooks will also be required for bioinformatics work in the lab. For each separate project, a dated ELN folder should be saved. Document general tasks performed related to each project. Do not replicate the entire script here, but provide links in a Google Doc to point others to the location of scripts, logs, results, etc. related to that work. This can be as simple as pointing to the other documentation types below.

### GitHub
GitHub repositories should be used for saving useful lab scripts. GitHub uses version control and branching, so changes over time can be viewed. This also enables other lab members (concurrent or future) to pull your code and use it for their applications. Keep repositories private until Jessi approves it for public sharing, as repositories in development should be reviewed prior to release. This should, however, be done for published work where sharing the repository can significantly aid reproducibility.

### R Markdown
R markdown is a handy way of tracking and integrating your R scripts with figures and table output. Use this to document the purposes of each step in your script and visualizing output. This can then be more easily followed by others.

### README Files
README files may be useful for analysis performed at command line, or where other metadata might be useful to capture. These README files should remain in the file structure with which they are associated so others will immediately see them.

### Jupyter Notebooks
Jupyter Notebooks are similar to R Markdown in that you can simultaneously annotate steps, show data output, and write code. Jupyter Notebooks are dynamic in that you can run the code and modify it within the notebook. It was developed for python, but works with a variety of languages/kernels.
