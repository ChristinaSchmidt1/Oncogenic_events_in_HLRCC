# Oncogenic_events_in_HLRCC

The notebook contains:
1. DESeq2 analysis and GSEA using HLRCC patients data comparing tumour versus normal published as part of the paper of Crooks et. al. 2021 (https://pubmed.ncbi.nlm.nih.gov/33402335/).
2. GSEA using transcriptomics data from mouse cells of Lorea Valcarcel-Jimenez et al (under revision).

## Reproducibility
Code for the R analysis can be reproduced by following the script in `Patients_GSE157256.Rmd` and `MouseCells.Rmd`. These include the DESeq2 analysis, GSEA and visualisations.

Signatures used for pathway analysis where downloaded from MSigDB (https://www.gsea-msigdb.org/gsea/msigdb) apart from `EMT-signature.csv`, which was downloaded directly from the publication of Taube et al. 2010 (https://pubmed.ncbi.nlm.nih.gov/20713713/), and safed in the folder `"Input_MSigDB_Signatures"`.

## Data
### Publicly available patients data:
The RNA-seq data of HLRCC patients were downloaded from the GEO database, under accession GSE157256 (https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE157256). Here we used the tumours/adjacent tissue samples (5 primary tumours and paired adjacent tissue). The downloaded input files can be found in the folder `"InputData_Patients_GSE157256"`:

1. `GSE157256_RSEM_counts.txt`
2. `SampleInfo_GSE157256.csv`

After performing DESeq2 analysis and GSEA the results are safed in the folder `"OutputData_Patients_GSE157256"`:

1. DESeq results:`DESeq_TvWT_Patients_GSE157256.csv`
2. GSEA results: `GSEA_result_KEGG-Hallmark-Reactome-Biocarta-NRF2-EMT_Patients_GSE157256.csv`

### Transcriptomics data Lorea Valcarcel-Jimenez et al:
The RNA-seq data of the mouse cells will be deposited with the manuscript and I will update this section and provide the accession number. Differential expression analysis has been performed by the Cambridge Genomic Services, Department of Pathology, University of Cambridge prior to this analysis and the details can be found in the file `NGS-L.Valcarcel-40680-report.html` proviced by the Cambridge Genomic Services and in the methods section of the manuscript of Lorea Valcarcel-Jimenez et al (under revision). Input data will be available upon publication in the folder `"InputData_MouseCells"`:

1.`.csv`

2.`.csv`

3.`.csv`

After performing GSEA the results will be safed in the folder `"OutputData_MouseCells`upon publication:

1.`.csv`

2.`.csv`

3.`.csv`

## Figures
Generated figures can be found in the html files or in the folders `"Figures_Patients_GSE157256"` and `"Figures_MouseCells"`
