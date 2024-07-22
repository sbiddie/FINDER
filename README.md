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

Datasources:

Dataset	Source	Version	Website	Genome build
DHS	ENCODE	Nov 23, 2021	https://www.meuleman.org/research/dhsindex/	Hg38
Footprints	ENCODE	OCT 20, 2020	https://www.vierstra.org/resources/dgf	Hg38
H3K27ac_GTRD	GTRD	v21.12	https://gtrd.biouml.org/#!	Hg38
ATAC-seq	GTRD	v21.12	https://gtrd.biouml.org/#!	Hg38
eRNA	PINTS	2021v1	https://pints.yulab.org	Hg38
ChIP-Seq	GTRD	v21.12	https://gtrd.biouml.org/#!	Hg38
GWAS Catalog	NHGRI-EBI	V1.0.2	https://www.ebi.ac.uk/gwas/docs/file	Hg38
ChIP-Seq_ASB	AD_ASTRA	V4.0.3	https://adastra.autosome.org/zanthar	Hg38
H3K27ac_dbInDel	dbInDel	v2018	http://enhancer-indel.cam-su.org	Hg19
CAV	ENCODE	OCT 20, 2020	https://www.vierstra.org/resources/dgf	Hg38
raQTL_MPRA	Primary_paper	NA	https://osf.io/w5bzq/wiki/home/?view	Hg19
caQTL	QTLbase	v1.3	http://www.mulinlab.org/qtlbase/studies.html	Hg19
CRISPRdel_CRISPRi	Primary_paper	NA	https://www.nature.com/articles/s41587-022-01211-7#MOESM3	Hg38
ATAC-seq	ATACdb	v1.03	https://bio.liclab.net/ATACdb/index.php	Hg38
ATAC-seq	ENCODE	v104	https://www.encodeproject.org	Hg19![image](https://github.com/user-attachments/assets/353ea026-d3e0-4d45-8362-ce3ac1da6c3b)

