Jacob Gutierrez
Lareau Lab 2024
gutierj6@mskcc.org


This project is a separate location to run cellphonedb using python. 

## Install

0.1) go to envs/ directory and follow the instructions to create a conda environemtn with the latest cellphonedb installation and dependencies. 

0.2) in a bash terminal spin up the jupyter notebook with `source spawn_notebook.sh`. This is required to interact with the `cpdb` conda environment and run the cellphone db analysis. 

0.2) In code/ directory run `00_DownloadDB_BuildDB.ipynb` to download and install the cellphonedb data base

Now youre ready to rumble

## Run Cellphonedb

1) For each dataset to be analyze be sure to prepare cellphone db output from seurat objects (if applicable)

2) Copy the `Cell-Cell_Interaction_Statistical_Method.ipynb` notebook and the update the input and output variables to correspond to the analysis you are interested in. I include example code chunks to preview the results to see if they are reasonable.

Note: This directory is using the vanilla statsitical method to identify interactions. Other options would include the DEG analysis method which may improve statistical significance due to limiting the genes of interest to those that are DEGs. 

3) Now use an Rmd notebook to visualize and analyze the resulting output and make pretty figures. 


## Result Analysis Notes

Theres gonna be a metric f*k ton of data coming out of this analysis. Far more than our glorified primate brains could comprehend or for a single graphic to visualize. 

I reccomend chosing specific cellular subsets to visualize in detail, i.e. epithelial cells are senders, what other celltypes (and their specific pathways) are most enriched and vice versa using epithelial cells are receivers.
However trying to extract specific interaction differences between donors, samples, or anatomical positions of the fallopian tube remains difficult. Anatomical positions would be best using current methods where we can use the isthmus as a 'control' and fimbria as a 'disease' and find the specific cell cell interaction pathways that are differentiatlly utilized in these cells. However getting down to the subtype resolution remains difficult. 

JG: July 2024, I had a discussion with a fellow phd student whose whole phd thesis is a novel cell cell interaction analysis method that competes with cellphonedb to get the scoop about the field. So far there are some methods that allow direct comparisons but you must designiate the groups before you even begin. Extracting differential results from multiple cell-cell interaction runs is impossible currently. Thus by analyzing a large atlas of healthy fallopian tubes with cellphonedb we cannot statistically correlate pathways with a seprate dataset of FFPE 10x flex besides literally stating epithelial cells in dataset A have this pathway and so does epithelial cells in dataset B. 



