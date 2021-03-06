---
layout: default
title:  'Precourse Material - scRNAseq course'
---

#### <img border="0" src="https://www.svgrepo.com/show/19652/maths-class-materials-cross-of-a-pencil-and-a-ruler.svg" width="40" height="40"> Precourse material
***

##### <img border="0" src="https://www.svgrepo.com/show/4795/installation-symbol.svg" width="20" height="20"> Installations

We have conda recipies for all R packages in one file and for the Scanpy tutorial in another. If you have never worked with conda before, please read the [conda instructions](conda_instructions.md).

OBS! Need to fix some paths in instruction.
Also info on Docker?

<br/>

##### <img border="0" src="https://www.svgrepo.com/show/20109/database.svg" width="20" height="20"> Dataset

We will run all tutorials with a set of 3 PBMC 10x datasets from the 10X Genomics website, with different types of library preps.

These can be fetched using commands:

```
mkdir data  
cd data
curl -O http://cf.10xgenomics.com/samples/cell-exp/3.0.0/pbmc_1k_v2/pbmc_1k_v2_filtered_feature_bc_matrix.h5
curl -O http://cf.10xgenomics.com/samples/cell-exp/3.0.0/pbmc_1k_v3/pbmc_1k_v3_filtered_feature_bc_matrix.h5
curl -O http://cf.10xgenomics.com/samples/cell-exp/3.0.0/pbmc_1k_protein_v3/pbmc_1k_protein_v3_filtered_feature_bc_matrix.h5
```

All code is written so that you stand in the folder where the scripts are when you run the code and fetch data from the data folder with path `../data/` and all output files goes into folder `../write/lab_name/` where `lab_name` can be either of `scran`, `scanpy` or `seurat`.

So also create the folder 'write' and subfolders for the lab you are planning to run.

```
 	cd ..
mkdir write
mkdir write/seurat
mkdir write/scran
mkdir write/scanpy
```

<br/>


##### <img border="0" src="https://www.svgrepo.com/show/17086/server-client-exchange.svg" width="20" height="20"> Uppmax

**Attention**: This step is no longer required for the course. It is only used in one of the lectures


1.   If you do not already have an Uppmax account, create and Uppmax account following these [instructions](files/Apply_for_Uppmax_account.pdf). OBS! It may take a few days to recieve the account, so proceed with this point as soon as possible.

2.   Log in to SUPR and request membership in the project g2019002. Account approval requires manual confirmation from the course organizers, so it may not happen immediately.

3.   Make sure you can connect to Rackham at Uppmax using a terminal. If you use a pc we recommend MobaXterm (http://mobaxterm.mobatek.net) or Windows 10 Bash for Linux.

4.   If you still feel uncertain how to work in a terminal please take time to do the first three parts in the “Unix tutorial for beginners” that can be found here http://www.ee.surrey.ac.uk/Teaching/Unix/ before the course starts. Otherwise you will not be able to take in the practical parts.  

5.   Make sure that you can read and write in the course folder by creating a file with your uppmax user name in the `/proj/g2019002/completed` folder. If you cannot write to the folder, the most likely reason is that you have not requested access to the course project via [SUPR](https://supr.snic.se/), see point 2. OBS! It may take an hour or so from the time your access is approved before you can actually write to the folder. We will check before the course that all students have logged in and done this, so do not forget!

6.  Install R on your own computer, instructions can be found [here](https://scilifelab.github.io/courses/r_programming/1703/precourse).  

7.  Install Rstudio on your own computer to run all your commands (This is optional). Rstudio is a very powerful GUI for structuring your R code in a good way.

8.  If you feel that you need to touch up on your R-skills before the course start, we recommend that you go through some basic tutorials before the course starts. A list of useful tutorials can be found [here](https://scilifelab.github.io/courses/r_programming/1703/precourse).

9.  In R install the programs listed below. We will work with several R programs during the course and it takes a while to install so if you can do it before you will not have to waste time installing during the exercise time.

*   SCDE package - [website](http://hms-dbmi.github.io/scde/package.html), [bioconductor](http://bioconductor.org/packages/release/bioc/html/scde.html)
*   Scater package - [website](https://github.com/davismcc/scater), [bioconductor](http://bioconductor.org/packages/release/bioc/html/scater.html)
*   SC3 package - [website](https://github.com/hemberg-lab/SC3), [bioconductor](https://bioconductor.org/packages/release/bioc/html/SC3.html)
*   SCRAN package - [website](https://github.com/elswob/SCRAN), [bioconductor](http://bioconductor.org/packages/release/bioc/html/scran.html)
*   Seurat package - [website](http://satijalab.org/seurat/install.html) - OBS! the exercises were designed for Seurat v2 and may not work with Seurat v3.
*   MAST package - [website](https://github.com/RGLab/MAST), [bioconductor](https://bioconductor.org/packages/release/bioc/html/MAST.html)
*   Monocle package - [website](http://cole-trapnell-lab.github.io/monocle-release/), [bioconductor](https://bioconductor.org/packages/release/bioc/html/monocle.html)   

OBS! If you run in to trouble during installations, please have a look at the troubleshooting pages for installations that most of the packages have. If you still do not succeed in installing them, please email to Åsa Björklund (asa.bjorklund at scilifelab dot se) and she will try to help you out if possible.
