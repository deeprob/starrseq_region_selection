# STARR-seq library region selection

To construct STARR-seq libraries, potential enhancer regions were selected based on chromatin signatures and TF binding sites.

**PS. This was originally prepared by Matt.**

# STEPS

1. Union of H3K4me1 and H3K27ac sites

2. Removal of 2kb TSS sites

3. Keep histones sites that intersect with at least 1 TF ChIP site in Hek cells or EP300 ChIP site in other cell lines

4. Pad less than 500 bp regions

# Output

Master file with a list of potential enhancer regions 

# Script descriptions

1. root/src/0_download_encode_data.py: Downloads Chip-Seq data of histones, TFs and p300 from encode in hek293/hela/k562 cell lines.
2. root/src/1_liftover_tcf7l2.py: TCF7L2 chip seq data was aligned to hg19 genome assembly. This script does liftover to hg38.
3. root/src/2_get_tss.py: Gets the genomic coordinates of TSSs of refseq genes.
4. root/src/3_create_master+list.py: This script follows the above steps and generates a list of regions to conduct STARRSeq on.
