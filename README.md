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
