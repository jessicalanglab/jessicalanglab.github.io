---
layout: page
title: Our Computing Platforms
description: Your guide to getting started
background: '/img/bg-about.jpg'
---
#### [Bioinformatics Docs](https://jessicalanglab.github.io/Resources/BioinformaticDocs) Table of Contents
+ [GitHub](https://jessicalanglab.github.io/Resources/BioinformaticDocs/GitHub)
+ [Computing platforms](https://jessicalanglab.github.io/Resources/BioinformaticDocs/ComputingPlatforms)
+ [Lab Pipelines](https://jessicalanglab.github.io/Resources/BioinformaticDocs/pipelines)
+ [Data Storage](https://jessicalanglab.github.io/Resources/BioinformaticDocs/storage)
+ [Electronic Lab Notebooks for Bioinformatics](https://jessicalanglab.github.io/Resources/BioinformaticDocs/notes)

## Where will you compute?
We use different computing resources depending on the job at hand.
1. Large-scale computing tasks: our BRC virtual machine (VM). This is what most of this documentation focuses on.
2. Small-scale computing tasks (i.e. most of our post-pipeline analysis): local machine (your Windows computer). See some notes toward the end of this page.

### BRC VM

#### Logging in
1. Ensure that you are either hard-wired (ethernet) connected on campus, or connected by VPN. Note that if you need to access our RestrictedDrive, you must be connected to the smph.vpn.wisc.edu VPN portal.
2. For computing, connect to the BRC VM in your command line app  
>`ssh brc12.secure.biotech.wisc.edu`  
3. You will be prompted for our lab's shared username and password. Please request this information from Jessi Lang or other members of the lab.

#### BRC VM structure
Upon login, you will automatically land at /home/BIOTECH/jlang. This is the home directory for our lab's VM where computing will take place. Note that this is a shared lab space, so please be respectful of others data.

BRC maintains extensive software available to all BRC server users (`/mnt/software`).

BRC also maintains many reference genomes (`/mnt/genomes`).

#### Data transfers
All data transfers on BRC VMs must be done within the data transfer server, which is a separate ssh login (same credentials):  
>`ssh brchome.ad.biotech.wisc.edu`

Our BRC VM account has a total of 1TB of space allocated, and thus is only meant for active use during analysis. Our long-term data storage is on the Lang Lab RestrictedDrive (aka ResearchDrive). To move data from RestrictedDrive to the BRC VM, you must use Globus.

*Note that Protected Health Identifiers (PHI) and other restricted data is not permitted on BRC VMs.*

To connect RestrictedDrive > Globus:
1. Navigate to [Globus](https://app.globus.org/) and sign in using your UW-Madison credentials.
2. Add the "wisc-restricted-kueck" collection in the File Manager tab using the Collection Search. You should now see the folder structure for our RestrictedDrive.
  + If you see an access denied message, you may want to first confirm that you have access to the RestrictedDrive. Instructions [here](https://kb.wisc.edu/researchdata/internal/page.php?id=93998#connect).
  + If you have access to the RestrictedDrive, but cannot access in Globus, you may need to be added to the collection. Email [Globus support](mailto:globussupport@wisc.edu).

To connect Globus > BRC VM account:
+ (TBD)

To transfer from BRC VM to your local machine, you must be in a directory on your local computer (i.e. not ssh'ed into BRC VM)  
>`scp jlang@brchome.ad.biotech.wisc.edu:path/to/file /path/to/your/local/folder`

#### BRC VM specs
+ 6 CPUs
+ 40GB of RAM
+ no workload manager available (i.e. slurm or others)

#### Software Installation

Similarly, for BRC server installations, you may find that some software requires higher-level permissions. Contact [BRC IT support](mailto:brc@biotech.wisc.edu).

### Local Computing environment
#### Software Installation
If installing software on your computer, you may run into issues with computer permissions based on required SMPH security protocols. If so, please contact [Dept of Pathology IT support](mailto:support@pathology.wisc.edu).

#### R & RStudio
A large amount of the software/packages we use for secondary analysis of genomic data uses R scripts and packages. These are most easily visualized in real time using the  RStudio program.

Recording notes in R Markdown (.rmd) format helps to document the analysis analogous to a lab notebook entry. We strongly encourage heavy use of markdown documentation for reproducibility, troubleshooting, refining, and documentation for publication.
