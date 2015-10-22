# ALEC
The Amplicon Long-read Error Correction 
ALEC (Amplicon Long-read Error Correction) was developed to correct sequencing and alignment errors [insertion/deletions (indels) and mismatches] generated by targeted amplicon sequencing derived from the PacBio RS platform. This script has been validated with full-gene sequencing of the CYP2D6 gene (ROI reads) generated by the PacBio RS II platform and according to the P5-C3 Pacific Biosciences protocol, and aligned with BWA MEM with parameter –x pacbio. ALEC may have utility for other genes, sequencing platforms, and/or chemistries; however, optimizing the correction parameters may be necessary to achieve ideal sequence correction and output for sequencing platforms and genes other than those that were validated and noted above. 

There are four types of sequencing errors that can be corrected after applying ALEC:
1) Random indels
2) Indels within homopolymers
3) Indels near sequence variants
4) Random mismatches

The ALEC script takes a fasta file as a reference file and a SAM file as the raw data alignment file, and automatically generates a corrected fasta file as output in the working directory. The usage of the script is as below:

Python ALEC.py input.sam reference.fasta

Note: the script only takes one single sequence as reference each time. 

The script was developed with Python 2.7.

For additional information on the development and validation of ALEC with the CYP2D6 gene, see Qiao W and Yang Y, et al. 2015, under review.

A manuscript detailing and evaluating the functionality of ALEC is currently in preparation.

