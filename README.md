# SABR
Workflow for Semi-automated background removal to normalise imaging mass cytometry data

The here provided pipeline & guide are part of the IMC normalisation methodology proposed in: <br/>
"Semi-automated background removal limits data loss and normalizes imaging mass cytometry data" by Ijsselsteijn ME, Somarakis A, Lelieveldt BP, Höllt T, de Miranda NF, Cytometry Part A. 2021 Dec;99(12):1187-97. https://doi.org/10.1002/cyto.a.24480 

<br/>

## Abstract
Imaging mass cytometry (IMC) allows the detection of multiple antigens (approximately 40 markers) combined with spatial information, making it a unique tool for the evaluation of complex biological systems. Due to its widespread availability and retained tissue morphology, formalin-fixed, paraffin-embedded (FFPE) tissues are often a material of choice for IMC studies. However, antibody performance and signal to noise ratios can differ considerably between FFPE tissues as a consequence of variations in tissue processing, including fixation. In contrast to batch effects caused by differences in the immunodetection procedure, variations in tissue processing are difficult to control. We investigated the effect of immunodetection-related signal intensity fluctuations on IMC analysis and phenotype identification, in a cohort of 12 colorectal cancer tissues. Furthermore, we explored different normalization strategies and propose a workflow to normalize IMC data by semi-automated background removal, using publicly available tools. This workflow can be directly applied to previously acquired datasets and considerably improves the quality of IMC data, thereby supporting the analysis and comparison of multiple samples. 


<br/>


## Use
Detailed step-by-step instructions are available in the [IMC_analysis_guidelines](/IMC_analysis_guidelines_SABR.pdf)

In short, raw IMC images are exported from the standard biotools/fluidigm MCD viewer as single-marker images and adapted to Ilastik-readable TIFF files using the 'Prepare_Images_for_Ilastik3' matlab script. 
Semi automated background removal (SABR) is performed for each marker using the 'Ilastik_Backgroundremoval.ilp' ilastik pipeline. The resulting output are binary tiff images where '0' corresponds to background and '1' to signal. these files can be directly combined with a cellsegmentation masks for downstream IMC analyses

<br/>


## Cite 
When using the methodology and/or pipeline for any publications, please cite: <br/>
Ijsselsteijn ME, Somarakis A, Lelieveldt BP, Höllt T, de Miranda NF. Semi‐automated background removal limits data loss and normalizes imaging mass cytometry data. Cytometry Part A. 2021 Dec;99(12):1187-97. 

