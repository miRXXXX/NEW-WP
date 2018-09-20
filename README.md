# Wepro
### 1. Introduction
miRTIGO is a novel miRNA target predictor, designed to identify sample-specific miRNA targets by  analyzing the same-sample miRNA-mRNA expression profiles. miRTIGO decomposes the biological procedure behind miRNA targeting into two independent stages: contacting and binding. Approximating the contacting stage by a random collision model, and the efficiency of the binding stage by sequence matching scores of RNAs, miRTIGO models endogenous RNA competition explicitly in a global scale and outputs an miRTIGO signature matrix to measure the relative activity of each individual miRNA-mRNA interactions.

#### 1.1 Publication
The publication for miRTIGO can be found [here](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1812-8)

#### 1.2 citation
Please cite:*xxxxxxxx*

---
### 2. Executing miRTIGO
####  2.1 Files required
miRTIGO is written in R. In order to run the current version of miRTIGO, the users should provide two data files describing the expression levels of each miRNA and mRNA in a sample, respectively. And one additional file describing the correspondence of samples between the miRNA and mRNA data files. All files are tab-delimited ASCII text files and must comply with the following specifications:

1.**Input miRNA/mRNA file** is organized as follows:<br>
![test](https://github.com/Henripan/Wepro/blob/master/input%20miRNA%20file.png)<br>
![test](https://github.com/Henripan/Wepro/blob/master/input%20miRNA%20file.png)<br>

The first line contains the labels Name followed by the identifiers for each sample in the dataset. <br>
>Line format: `Name(tab)(sample 1 name)(tab)(sample 2 name)(tab)...(sample N name)`<br>
>Example: `Name	sample_1	sample_2	sample_3	...	sample_10`<br>

The remainder of the file contains data for each of the miRNAs/mRNAs. There is one line for each miRNA/mRNA.Each line contains the miRNA/mRNA name and a value for each sample in the dataset.<br>

2.**Sample-to-sample file** generally contains three columns and is organized as follows:<br>
![test](https://github.com/Henripan/Wepro/blob/master/input%20miRNA%20file.png)<br>
The first line contains the labels Name followed by the identifiers for each sample in the dataset. <br> 

>Line format: `Name(tab)(sample name in miRNA file)(tab)(sample name in mRNA file)`<br>
>Example: `Name	sample_1	sample_a`<br>

The remainder of the file contains data for each of the mRNAs. There is one line for each mRNA.Each line contains the mRNA name and a value for each sample in the dataset.

#### 2.2 Script Execution<br>

refer to R
