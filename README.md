# Transana
Transcript level expression analysis using Drosophila RNA-seq data

## Salmon-tximport-DESeq2 pipeline
* Description<br>
Salmon is used to generate transcript-level expression, and tximport is a tool to estimated counts (gene-level or transcript-level) based on transcript-level abundance (from salmon). The counts can be used in the following DESeq2 analyses, so that differentially expressed genes or transcripts can be identified statistically.<br>
Here I used  
* Data source<br>
Yang et al. 2018 https://doi.org/10.1101/350363<br>
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE99574<br>

* References<br>
salmon:<br>
https://combine-lab.github.io/salmon/<br>
tximport:<br>
https://bioconductor.org/packages/release/bioc/html/tximport.html<br>
manuscript:<br>
https://f1000research.com/articles/4-1521/v1<br>





