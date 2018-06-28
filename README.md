# Transana
Transcript level expression analysis using Drosophila RNA-seq data

## Salmon-tximport-DESeq2 pipeline
* Description<br>
    Traditional DESeq2 gene-level analysis is insensitive to discover isoform-level differential expression. For instance, it is well known that the found in neurons (fne; FBgn0086675) gene have different enrichment of isoform between female and male head (Sun et al. 2015; PMID:26511498), but such sexual difference cannot be identified using traditional DESeq2 gene-level analysis (padj = 0.21 for fne locus).  We are interested if the improved Salmon-tximport-DESeq2 pipeline could identify such difference.  Specifically, salmon is used to generate transcript-level expression, and tximport is a tool to estimated counts (gene-level or transcript-level) based on transcript-level abundance (from salmon). The counts can be used in the following DESeq2 analyses, so that differentially expressed genes or transcripts can be identified statistically. Indeed, we identified significant enrichment of fne-a (male) and fne-b (female) isoforms using the salmon-tximport-DESeq2 pipeline, suggesting that the new pipeline is more advantageous than the traditional DESeq2 pipeline to identify differential expression at the isoform-level. <br>

* Data source<br>
Yang et al. 2018 https://doi.org/10.1101/350363<br>
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE99574<br>

* References<br>
salmon:<br>
https://combine-lab.github.io/salmon/<br>
tximport:<br>
https://bioconductor.org/packages/release/bioc/html/tximport.html<br>
https://f1000research.com/articles/4-1521/v1<br>
fne gene manuscript<br>
http://www.g3journal.org/content/ggg/5/12/2865.full.pdf<br>

* R Script


* Sex-biased expression of two fne isoforms<br>
![alt text](https://s3.us-east-2.amazonaws.com/haiwangyang.com/image/fne.png)

