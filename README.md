# ALEC
Amplicon Long-read Error Correction 
(ALEC) was developed to correct sequencing and alignment errors [insertion/deletions (indels) and mismatches] generated by targeted amplicon sequencing derived from the PacBio RS platform. This script has been validated with full-gene sequencing of the CYP2D6 gene generated by the PacBio RS II platform and according to the P6-C4 Pacific Biosciences protocol. Utility of ALEC for other genes was evidenced by a 9.2kb PacBio sequencing of RYR2 gene. ALEC may have utility of other sequencing platforms (such as Oxford Nanopore), and/or other sequencing chemistries; however, optimizing the correction parameters would be necessary to achieve ideal sequence correction and output for genes and sequencing platforms other than those that were validated and noted above. 

Four types of sequencing errors can be corrected after applying ALEC: 1) random mismatches; 2) random indels; 3) indels within homopolymers; and 4) indels near sequence variants.
 
The ALEC script takes a fasta file as a reference file and a SAM/BAM file as the raw data alignment file, and automatically generates a corrected fasta file as output in the working directory. The usage of the script is as below:

Python ALEC.py input.sam reference.fasta

Note: 1) The script only takes one single sequence as reference each time. Please use the exact interval of sequenced genomic region as reference. 2) We do not have a preference regarding the available sequence alignment tools; however, we used SAM files generated with BWA-MEM (0.7.12) to develop the ALEC script (see reference below for details).

The script was developed with Python 2.7.

For additional information on the development and validation of ALEC with the CYP2D6 gene, see reference: Qiao W and Yang Y, et al. Hum Mutat. 2016 Mar;37(3):315-23. doi: 10.1002/humu.22936. Epub 2015 Dec 18.

A manuscript detailing and evaluating the functionality of ALEC is currently in preparation.

## System requirements
  * Python 2.7.10
  * asgparse
  * pysam
* sys
* re
* time
* random
* itertools
* operator
* math
* numpy
