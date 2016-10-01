---
layout: project
title: 10X Genomics
---

I have been at [10X Genomics](http://www.10xgenomics.com) since October 2014, when we were still stealth. My projects have been primarily on the DNA sequencing platform using molecular barcodes attached in emulsion to add long range genetic information to short read nextgen sequencing.

### OVERVIEW

<img src="../projects/overview.jpg" alt="10X Genomics technology" style = "align:center" >

The 10X platform starts with high molecular weight DNA input into a microfluidic system which partitions those long DNA molecules into "GEMs" (Gel bead in emulsion) with oil surrounding an aqueous solution containing the DNA and reagents surrounding a gel bead containing millions of copies of the same barcode DNA sequence. Each different gel bead has a different barcode DNA oligo with high probability. Each GEM gets roughly 10 long DNA molecules. So when you map the reads from a single barcodes, they cluster into a few small regions of the genome associated with their molecule of origin. 

This can be done for either whole genome or targeted sequencing while retaining the linked read long range information.
<img src="../projects/genomeexome.jpg" alt="WGS or WES 10X linked reads" style="align:center">

### PHASING LONG MOLECULES

<a href="http://www.10xgenomics.com/applications">
<img src="../projects/hetdel.jpg" alt="10X Het Deletion" style="float:left;height:250px;margin: 0 20px 20px 0;" class="img-rounded">
</a>

The 10X platform can also be used for DNA sequencing. Instead of single cells, the sample is partitioned into long molecules (mean ~50kb and up to ~250kb), which are used to produce short reads with a barcode denoting the molecule of origin. The barcodes allow downstream analyses to "link" reads together according to their source molecules. Linked reads provide useful long-range information that can disambiguate between homologous regions and enable haplotype phasing across large chunks of chromosomes.

I’ve made significant contributions to the development of [Long Ranger](http://support.10xgenomics.com/genome-exome/software/pipelines/latest/what-is-long-ranger), our pipeline for analyzing 10X genome and exome data. I’ve also contributed to the design and analysis of a custom exome bait set that takes advantage of linked reads to improve phasing of genes.
