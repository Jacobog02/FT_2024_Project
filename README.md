# FT_2024_Project
Repository for the reproducible analysis of [Title]{Single Cell and Spatial Atlas of Healthy Fallopian Tube and Premalignant Lesions}.

This directory contains sub directories that contains analyses of various datasets or processes. 

Currently sub directories include: 

1) FT_Atlas directory which contains the reproducible analysis of fresh + FFPE Fallopian tube atlas. 

  > This contains code,data,output with labeled scripts in code to run in serial to reproduce this analysis. 
  > Note that the data directory is not fully uploaded to github due to size limits and may migrate to a seperate large data directory 
  > Records for what single cell data was extracted and processed is present in /FT_Atlas/data/public_aligned_data 
  
Other notes for the Atlas analysis, 
* scRNA data generated from this study resides in `/FT_Atlas/data/study_5_h5s`
* Nanostring CosMx SMI data generated from this study resides in `/FT_Atlas/data/resegmented_data`
* Relevant Supplemental material resides in `Lengyel_supp` or `ulrich_supp` in the data directory 
* LARGE DATASETS CANNOT BE UPLOADED TO GITHUB AND WILL BE MOVED AT SOMEPOINT

2) `FT_cellphonedb` directory contains reproducible analysis of cell-cell interaction via CellphoneDB

  > This again contains code,data,output to largely automate these analyses and then export the results back to the relevant subanalysis. 
  > This directory is mostly to record how this specific version of cellphoneDB was installed and run for this analysis and how cellphonedb can be implemented in the future. 
  
  

  
  

