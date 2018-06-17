---
layout: project
title: 10X Genomics
---

I worked at [10X Genomics](http://www.10xgenomics.com) between October 2014, when they were still stealth, and May 2017. My projects were primarily on the DNA sequencing platform using molecular barcodes attached in emulsion to add long range genetic information to short read nextgen sequencing.

### OVERVIEW

<img src="../projects/overview.jpg" alt="10X Genomics technology" style = "align:center" >

The 10X platform starts with high molecular weight DNA input into a microfluidic system which partitions those long DNA molecules into "GEMs" (Gel bead in emulsion) with oil surrounding an aqueous solution containing the DNA and reagents surrounding a gel bead containing millions of copies of the same barcode DNA sequence. Each different gel bead has a different barcode DNA oligo with high probability. Each GEM gets roughly 10 long DNA molecules. So when you map the reads from a single barcodes, they cluster into a few small regions of the genome associated with their molecule of origin. This long range information can then be used to map into repeat regions of the genome, phase haplotypes, and call structural variation.

This can be done for either whole genome or targeted sequencing while retaining the linked read long range information.
<img src="../projects/genomeexome.jpg" alt="WGS or WES 10X linked reads" style="align:center">

### MAPPING REPEAT REGIONS OF THE GENOME

<img src="../projects/repeatmapping.jpg" alt="Mapping repeat regions of the genome confidently using 10X genomics molecular barcodes" style="float:right; height:250px;margin: 0 20px 20px 0;" class="img-rounded">
This long range genetic information allows us to map into repeat regions 
of the genome using either flanking unique sequence as in the case or short exact repeats or rare interspersed differences typical of longer 
segmental duplications. Segmental duplications are increasingly being recognized as the source of new gene creation as well as gene dosing variation. 
You can read more about this method on my <a href="../projects/lariat.pdf">white paper</a>. I was lead on this project and presented my findings 
at Genome Informatics in September 2016. My poster is <a href="../projects/GIposter.pptx">here</a>.

### PHASING LONG MOLECULES

<a href="http://www.10xgenomics.com/applications">
<img src="../projects/hetdel.jpg" alt="10X Het Deletion" style="float:left;height:250px;margin: 0 20px 20px 0;" class="img-rounded">
</a>

The 10X platform can also be used for haplotype phasing. Because there are so many partitions/barcodes and each barcode has so few DNA molecules, the chance that a barcode has 2 molecules from the same locus in the genome but opposite haplotypes is vanishingly small. Based on this, for each cluster of reads on the genome from one barcode, the chances that all of those reads come from the same haplotype is exceedingly high. We can use this long range information to link alleles from multiple heterozygous variants into haplotypes. Then more molecules can link those alleles to even more alleles and proceeding this way we can create phase blocks that span megabases or even whole chromosome arms. 

I contributed to the phasing algorithm and extended it from phasing variants to phasing molecules and all of their reads. With this information it makes normally difficult to call variant types like heterozygous deletions much easier. I also designed and implemented an algorithm to use the phasing to filter false positives that do not segregate on haplotype lines. In this same algorithm I can correct genotypes of variants that were falsely called heterozygous which were in reality homozygous. The details of this algorithm can be found on our <a href="../projects/phasing10x.pdf">phasing white paper</a>.
