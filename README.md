# FineMap

Fine mapping pipeline 
----------------------
Sourya Bhattacharyya

La Jolla Institute for Immunology, La Jolla, CA 92037, USA

Fine mapping of the GWAS summary statistics.

Implements a wrapper for the FINEMAP package 
(http://www.christianbenner.com/)

Note: Currently the package supports GWAS files with respect to the reference genome hg19 

For GWAS files with hg38 reference genome configuration, users are requested to first use 
the liftover tool (https://genome.ucsc.edu/cgi-bin/hgLiftOver) to convert the genomic coordinates 
from hg38 to hg19.

Running the script
==================

First edit the configuration file (configfile).

## Note: the pipeline supports using LocusZoom (http://locuszoom.org/) to plot every fine mapped 
GWAS loci. However, execution of LocusZoom takes a long time. So, we recommend to not use it during fine 
mapping, but use it separately to plot selected fine mapped GWAS loci.

Once the configuration file is edited, run the script 
qsub_finemap_job.sh

It will invoke the finemap executable along with the corresponding configuration file.

Output
========

With respect to the specified output directory (parameter "OutDir")
check the folder "sss"

FINAL_summary_credible_set.txt : File containing the GWAS loci, credible causal sets and the corresponding SNPs.

FINAL_top_snp_credible_set.txt: All the SNPs listed in the credible causal sets. 


Contact
==========

For any queries, please create an issue and we'll respond. Otherwise, please e-mail

Sourya Bhattacharyya: sourya@lji.org

Ferhat Ay: ferhatay@lji.org





