# Oncogenic_events_in_HLRCC
This notebook includes the code and analysis done for the publication ["HIRA loss transforms FH-deficient cells" published in science advances in 2022](https://www.science.org/doi/10.1126/sciadv.abq8297).

The notebook contains:
1. DESeq2 analysis and GSEA using HLRCC patients data comparing tumour versus normal published as part of the paper of [Crooks et. al. 2021](https://pubmed.ncbi.nlm.nih.gov/33402335/).
2. GSEA using transcriptomics data from mouse cells of [Lorea Valcarcel-Jimenez et al](https://www.science.org/doi/10.1126/sciadv.abq8297).
3. Transcription factor (TF) analysis using transcriptomics data from mouse cells of [Lorea Valcarcel-Jimenez et al](https://www.science.org/doi/10.1126/sciadv.abq8297).

## Reproducibility
Code for the R analysis can be reproduced by following the script in `Patients_GSE157256.Rmd`, `MouseCells.Rmd` and `TranscriptionFactorAnalysis.Rmd`. These include the DESeq2 analysis, GSEA, TF analysis and visualisations.

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
The RNA-seq data of the mouse cells are deposited  in Gene Expression Omnibus (GEO) database under accession number GSE201992. Differential expression analysis has been performed by the Cambridge Genomic Services, Department of Pathology, University of Cambridge prior to this analysis and the details can be found in the file `NGS-L.Valcarcel-40680-report.html` provided by the Cambridge Genomic Services and in the methods section of the manuscript of [Lorea Valcarcel-Jimenez et al](https://www.science.org/doi/10.1126/sciadv.abq8297). Input data are be available in the folder `"InputData_MouseCells"`:

1.`Results_gc_length_corrected_Cl19__VS__Cl19_gHira.csv`
2.`Results_gc_length_corrected_Fl__VS__Fl_gHira.csv`
3.`Results_gc_length_corrected_Fl__VS__Cl19.csv`

After performing GSEA the results are safed in the folder `"OutputData_MouseCells`:

1.`GSEA_result_KEGG-Hallmark-Reactome-Biocarta-NRF2-EMT_HIRAvCL19_.csv`
2.`GSEA_result_KEGG-Hallmark-Reactome-Biocarta-NRF2-EMT_HIRAvsFL_.csv`
3.`GSEA_result_KEGG-Hallmark-Reactome-Biocarta-NRF2-EMT_CL19vFL_.csv`

After performing the TF analysis the results are be safed in the folder `"OutputData_TF-Analysis`:

1. `TF-Analysis_HIRAvCL19.csv`
2. `TF-Analysis_FlxvCL19.csv`

## Figures
Generated figures can be found in the html files or in the folders `"Figures_Patients_GSE157256"` and `"Figures_MouseCells"`
