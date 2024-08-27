Jacob Gutierrez


I really need to organize all the previous scRNA FT studies and their corresponding files with scRNA data 



# Hu2020_study1

https://pubmed.ncbi.nlm.nih.gov/32049047/

Hu Z, Artibani M, Alsaadi A, Wietek N, Morotti M, Shi T, Zhong Z, Santana Gonzalez L, El-Sahhar S, Carrami EM, Mallett G, Feng Y, Masuda K, Zheng Y, Chong K, Damato S, Dhar S, Campo L, Garruto Campanile R, Soleymani Majd H, Rai V, Maldonado-Perez D, Jones S, Cerundolo V, Sauka-Spengler T, Yau C, Ahmed AA. The Repertoire of Serous Ovarian Cancer Non-genetic Heterogeneity Revealed by Single-Cell Sequencing of Normal Fallopian Tube Epithelial Cells. Cancer Cell. 2020 Feb 10;37(2):226-242.e7. doi: 10.1016/j.ccell.2020.01.003. PMID: 32049047.


> JG: Smart-seq2 chemistry so each cell has its own flipping i5 index aka fastq file. MIGHT be able to integrate but its like 200 cells ya feel

Cancer: GSE132149
Benign: GSE139079


# Dihn2021_study2

https://pubmed.ncbi.nlm.nih.gov/33852846/

Dinh HQ, Lin X, Abbasi F, Nameki R, Haro M, Olingy CE, Chang H, Hernandez L, Gayther SA, Wright KN, Aspuria PJ, Karlan BY, Corona RI, Li A, Rimel BJ, Siedhoff MT, Medeiros F, Lawrenson K. Single-cell transcriptomics identifies gene expression networks driving differentiation and tumorigenesis in the human fallopian tube. Cell Rep. 2021 Apr 13;35(2):108978. doi: 10.1016/j.celrep.2021.108978. PMID: 33852846; PMCID: PMC10108902.

scRNA: GSE151214



# Ulrich2022_study3


https://pubmed.ncbi.nlm.nih.gov/35320732/

Ulrich ND, Shen YC, Ma Q, Yang K, Hannum DF, Jones A, Machlin J, Randolph JF Jr, Smith YR, Schon SB, Shikanov A, Marsh EE, Lieberman R, Gurczynski SJ, Moore BB, Li JZ, Hammoud S. Cellular heterogeneity of human fallopian tubes in normal and hydrosalpinx disease states identified using scRNA-seq. Dev Cell. 2022 Apr 11;57(7):914-929.e7. doi: 10.1016/j.devcel.2022.02.017. Epub 2022 Mar 22. PMID: 35320732; PMCID: PMC9007916.

scRNA: GSE178101

cellxgene: https://cellxgene.cziscience.com/collections/fc77d2ae-247d-44d7-aa24-3f4859254c2c

10x 3' and DROP-seq 


>For scRNA-seq read count data, cells were selected with 1) the cell size factor and integrity filter: cells with >500 detected genes and with <10% mitochondria transcripts were kept (N=60,035 for 4 healthy subjects, and 17,905 for 2 diseased subjects); 2) the doublets filter: cells in a cluster that corresponded to doublets from 2 distant clusters in the global clustering (N=297 for 4 healthy subjects, and 107 for 2 diseased subjects) were removed. In all there were 59,738 cells for the 4 healthy human fallopian tubes with an average of 2,603 detected genes and 10,530 UMIs per cell; and 17,798 cells for the 2 diseased fallopian tubes with an average of 2,780 detected genes and 11,683 UMIs per cell. For each cell, raw transcript counts were normalized by (1) dividing by the total number of UMIs per cell and (2) multiplying by 10,000 to obtain a transcripts-per-10K measure, and then log-transformed by E=ln(transcripts-per-10K+1). For some downstream analyses, the normalized gene expression matrix was standardized for genes by centering and scaling for each gene using (E-mean(E))/sd(E).

#Lengyel2022_study4 

https://pubmed.ncbi.nlm.nih.gov/36543131/

Lengyel E, Li Y, Weigert M, Zhu L, Eckart H, Javellana M, Ackroyd S, Xiao J, Olalekan S, Glass D, Iyer S, Krishnan R, Bilecz AJ, Lastra R, Chen M, Basu A. A molecular atlas of the human postmenopausal fallopian tube and ovary from single-cell RNA and ATAC sequencing. Cell Rep. 2022 Dec 20;41(12):111838. doi: 10.1016/j.celrep.2022.111838. PMID: 36543131.

scRNA: https://cellxgene.cziscience.com/collections/d36ca85c-3e8b-444c-ba3e-a645040c6185a


>>> we require cells expressing at least 200 gene features and each gene feature present in at least 3 cells; 2) we remove doublets and triplets identified by DoubletDecon48
; 3) cells with ≥20% mitochondrial contents were filtered out as poor-quality cells with low viability. Each UMI count matrix, with cells from a certain anatomical site of a donor, is log-normalized using a procedure57
implemented with Seurat49


> Then the raw sequencing reads were aligned to the human reference genome hg38 and then filtered and quantified as UMI counts using barcode information via cellranger count. We further applied the following QC criteria to the UMI count matrix using an in-house pipeline: 1) we require cells expressing at least 200 gene features and each gene feature present in at least 3 cells; 2) we remove doublets and triplets identified by DoubletDecon48
; 3) cells with ≥20% mitochondrial contents were filtered out as poor-quality cells with low viability. Each UMI count matrix, with cells from a certain anatomical site of a donor, is log-normalized using a procedure57
implemented with Seurat49
function NormalizeData and FindVariableFeatures. Cells from different samples were integrated using Seurat function FindIntegrationAnchors,58
where top 2,000 highly variable gene features expressed across cells were used as anchors for pairwise sample integration. Prior to dimensionality reduction, a linear transformation scaling procedure was applied to remove unwanted variations. We performed dimensionality reduction using both PCA and UMAP. Shared nearest-neighbor (SNN) graph was constructed for graph-based clustering via Seurat function FindNeighbors and FindClusters correspondingly, at resolution of 0.5 for a relatively dense clustering.



