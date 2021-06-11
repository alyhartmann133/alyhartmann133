#_CesA_ Genes in Mosses
##Composition of scripts to analyze _CesA_ gene presence


This is a current project I am working on with Dr. Schwartz and Dr. Roberts at URI, along with other lab members. I am very interested in how these genes suggest early diversification within mosses and hope to explain how we were able to gather our results. This is still a work in progress, so please keep that in mind. :)

Within this repository there are two steps each with their own set of instructions and scripts. 
Prior to step one, one must gather their sequence data from wherever they source, but my sequence data consists of moss genomes and transciptomes from the **European Nucleotide Archive**. For this, reads can either be paired or singled, but if paired they must **ALWAYS** be kept together, and if one is deleted so must the other. 
- Additionally, for this analysis a reference genome will also be necessary, and for mine the reference genome was downloaded as a GFF file from **CoGe** and was further filtered for the 7 _CesA_ gene ID's found on **Phytozome**. 

Once all data has been gathered and downloaded you can proceed to step one which includes three scripts: _trim, align_, and _intersect_. These three scripts will filter through the downloaded fastq.gz files and adapt trim the reads, align to a reference genome, and then extract any reads aligning to the _CesA_ gene location, as identified in the GFF. By the end of step one, these three scripts done in the order of trim, align, intersect, should produce bam files with all gene locations, showing chromosome number, score of alignment, and the number of alignments present. 

Step two consists of two scripts that will take this findings and filter the results for better analysis. There is a _CesA_ and _processCesA_ script. 
