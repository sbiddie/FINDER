The datasets found in this package accompany Biddie et al. DNA-binding factor footprints and enhancer RNAs identify functional non-coding genetic variants.
doi: https://doi.org/10.1101/2023.11.20.567860

The files supplied consist of merged datasets (using Bedtools merge) in BED format. 
We present these files as merged files to reduce computational burden and remove presumptions of cell or tissue type when comparing multiple annotation types. 

Sources of datasets can be found in supplementary table 1 in the original Manuscript. 

All files are aligned to the human genome Hg38.

Users can interrogate a list of candidate non-coding genetic variants as BED format by using Bedtools intersect (https://bedtools.readthedocs.io/en/latest/content/tools/intersect.html).  

bedtools intersect [OPTIONS] -a <variant_file> -b <merged_annotation_file> 

We recommend the variant list as the first dataset (-a). 
When generating candidate non-coding genetic variant, preserving rsID and keeping these in the output file using OPTIONS in Bedtools intersect (such as -wo), will allow further downstream analysis. For example, deconvolution using FORGE2 (which requires rsID).

This approach is intended to be the least computationally burdensome approach, and therefore utilizes existing pipelines. 

The FINDER framework presented in the manuscript recommends intersecting candidate non-coding genetic variant lists (either lead variants alone or those in linkage disequilibrium) with the enhancer RNA (merged_eRNA) and DNase Footprint (merged_Footprint) files. The intersected candidate list can then be used downstream to infer function such as cell-type or transcription factor binding.


