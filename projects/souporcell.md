---
layout: project
title: souporcell
---

### Overview - single cell sequencing

<img src="../projects/singlecelloverview2.png" alt="10X Genomics single cell RNAseq" style = "align:center" >

### Souporcell

<img src="../projects/fig1.jpg" alt="souporcell" style = "align:center" >

Multiplexing different individuals' cells into a single cell RNAseq experiment has many advantages as an experimental design primarily because it removes batch 
effects between samples but is also valuable for reducing cost per donor, providing information on both cross-genotype doublets and the amount of ambient RNA 
in the experiment. By using variants detected in scRNA-seq reads, it is possible to assign cells to their donor of origin and identify cross-genotype doublets 
that may have highly similar transcriptional profiles, precluding detection by transcriptional profile. More subtle cross-genotype variant contamination can be 
used to estimate the amount of ambient RNA. Ambient RNA is caused by cell lysis before droplet partitioning and is an important confounder of scRNA-seq analysis. 
Souporcell is a method to cluster cells using the genetic variants detected within the scRNA-seq reads.
