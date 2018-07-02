# Transana
Transcript level expression analysis using Drosophila RNA-seq data

## Salmon-tximport-DESeq2 pipeline
* Description<br>
    Traditional DESeq2 gene-level analysis is insensitive to discover isoform-level differential expression. For instance, it is well known that the found in neurons (fne; FBgn0086675) gene have different enrichment of isoform between female and male head (Sun et al. 2015; PMID:26511498), but such sexual difference cannot be identified using traditional DESeq2 gene-level analysis (padj = 0.21 for fne locus).  We are interested if the improved Salmon-tximport-DESeq2 pipeline could identify such difference.<br><br>
    Specifically, salmon is used to generate transcript-level expression, and tximport is a tool to estimated counts (gene-level or transcript-level) based on transcript-level abundance (from salmon). The counts can be used in the following DESeq2 analyses, so that differentially expressed genes or transcripts can be identified statistically. Indeed, we identified significant enrichment of fne-RC (female) and fne-RD (male) isoforms using the salmon-tximport-DESeq2 pipeline, suggesting that the new pipeline is more advantageous than the traditional DESeq2 pipeline to identify differential expression at the isoform-level. <br>

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

* R Script and data structure<br>
** main script<br>
transana/tximport.Rmd<br>
** main data folder<br>
transana/data/<br>
** main output folder<br>
transana/output/<br>
** test script<br>
transana/tximport_testdata.Rmd<br>
** test data folder<br>
transana/testdata/<br>
It has the same data strucutre as transana/data/, but I only kept the minimum data for testing purpose.<br>
transana/testdata/dmel.design is experiment design file (for DESeq2)<br>
transana/testdata/dmel.FBgn2FBtr is a look-up table connecting FBgn and FBtr<br>
transana/testdata/dmel.FBgn2symbol is a look-up table connecting FBgn and symbol<br>
transana/testdata/dmel.tx2gene is a look-up table connecting transcript and gene ID (based on YO or FB annotation)<br>
transana/testdata/dmel.tx2ortholog is a look-up table connecting orthologs<br>
transana/testdata/salmon/ has salmon data (YO: YangOliver annotation)<br>

* Overall picture of transcript level MAplots<br>
Red, black, and blue dots are female-, un-, and male-biased expressed transcripts<br>
![alt text](https://s3.us-east-2.amazonaws.com/haiwangyang.com/image/transMAplots.png)<br>

* Sex-biased expression of two fne isoforms<br>
![alt text](https://s3.us-east-2.amazonaws.com/haiwangyang.com/image/fne.png??)<br>

