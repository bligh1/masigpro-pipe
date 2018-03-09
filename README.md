# maSigPro - pipeline

## Prerequisites
### Data object
Within the gene count data frame, the row names should be an array of gene names, and the column names should be a 
array of the individual observation points per time per replicate.

### Experimental Design Object
The experimental design data frame will contain (2 + # of groups) columns not including the row names. The row names
should be the same array of observation time points as the column names in the data object. It is required that the
order remains consistent. The first official column of the edesign object should be the time points corresponding to
the observation row. 

The second column should be the replicate identifier. Each replicate under a single group and time point should be
categorized under one number.
 
## Installing
The maSigPro pipeline will automatically install and load the necessary 'maSigPro' package

## Example
User can run the maSigPro piepline using the example data, edesign, and conversion files provided in the repository.
Currently, the pipeline requires 6 arguments following the executable command.

	1. data: rpkm3942modified3.txt
	2. edesign: edesign3942modified3.txt
	3. minimum observation threshold: 6
	4. step method: backward
	5. extraction scale: all
	6. conversion IDs: MacaqueGene.txt
 
After a few minutes, the pipeline should write a text file containing the significant genes identified. 
In this file, the first column will be the significant genes pre-conversion, the second column will be 
the significant genes pre-conversion that have a conversion target, and the third column will be the 
significant genes post-conversion. 

