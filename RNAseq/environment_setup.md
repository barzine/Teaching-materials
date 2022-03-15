# Setting up the environment for the differential expression analysis of bulk RNAseq data

Nowadays, many tools are used for differential expression analyses. We will focus on methods implemented in R.
The setup can be broken into four steps:
1/ Install R
2/ Install Rstudio
3/ Launch Rstudio and install Bioconductor
4/ Install DESeq2
5/ Optional useful packages.

## 1- To install R on your computer:
Please follow the instructions for your os:
Windows: https://cran.r-project.org/bin/windows/base/
macOS: https://cran.r-project.org/bin/macosx/
Linux (Ubuntu) : https://cran.r-project.org/bin/linux/ubuntu/fullREADME.html

There are other ways to install through [conda](https://docs.conda.io/en/latest/)/[bioconda](https://bioconda.github.io) (all platforms), [homebrew](https://brew.sh/) (macOS), if you are familiar with these packages managers, I believe you can also figure out how to install with them.

## 2- Install Rstudio
While [R](https://cran.r-project.org/) can be used without any specific IDE (integrated development environment),
I recommend trying the [Rstudio desktop one](https://www.rstudio.com/products/rstudio/#rstudio-desktop), especially for new users.
The free version is more than enough for personal use.

## 3 - Install Bioconductor
The next step can take quite a long time, and it requires an internet connection.

a) Launch Rstudio or R
b) In the console panel (it should be the left bottom panel), you should see the R version you have installed plus several other information such as R is free software, etc.
c) After the prompt (">"), type: 
```r
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(version = "3.14")
```

## 4 - Install DESeq2 
After having installed Bioconductor, you have to install DESeq2:

```r
#If you are in the same session than the previous step, you can skip the next two lines
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("DESeq2")
```

To test your installation:
```r
library(DESeq2)
```
You should see a lot of messages being printed out on your console and then: 

```r
vignettes("DESeq2")
```
You should have the vignette (sort of guided manual) of the DESeq2 package.

## 5 - Other useful optional packages to install are:

```r
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install(c("mixOmics","reshape2","tidyverse","ggplot2",
                       "tximport","tximportData","pasilla", "airway",
                       "reshape2"))
``` 
