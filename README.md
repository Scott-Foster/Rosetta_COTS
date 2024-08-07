---
output: github_document
bibliography: /home/fos085/zoteroFiles/JabRefPDF/SDFReferences.bib
csl: /home/fos085/ABARES/RISDM_MS/ecography.csl
---

## RosettaCOTS: translation between methods for measuring COTS and Coral Cover

## Summary

RosettaCOTS is an R package that provides the results of a calibration exercise between different methods for measuring COTS and coral cover. Its main function COTS_calibrate is a tool that predicts one measure from another, along with prediction and confidence intervals. RosettaCOTS is built upon data obtained in a CCIP-D2 field trip. It presents the results, in a useful manner, of all pair-wise models of all of the methods that measure COTS and all of the methods that measure coral cover. The COTS measurement methods are:

* Cull: performed by the Pacific Marine Group's (PMG's) professional cull team. Measures number of COTS culled and the dive time.
* Manta Tow: performed by the PMG's cull team. Measures of scars and tow distance. Note that the number of COTS seen has not been incorporated into this calibration (not enough COTS seen in the field trip).
* SALAD: performed by a JCU team, developers and experts in the method. Measures number of COTS seen and the number of Scars seen (that weren't associated with a COTS). Whilst a number of different effort metrics are available, we use swept area (unit of metres-squared).
* eDNA (concentration): performed by an AIMS team, developers and experts in the method. This measure is the concentration (quantitative measure) from the PCR assay. We note that there is a hierarchy to this sampling, there are multiple samples at a site and each sample has two technical (lab) replicates.
* eDNA (proportion): As eDNA (concentration), except that the measure is dichotomous (presence/absence of COTS eDNA in an assay). This is accumulated, to the site level, by taking the proportion of positives at a site. Strictly speaking this is an average (over samples) of averages (over technical replicates).

The coral cover measurement methods are:

* ReefScan-Transom: performed by an AIMS team, developers and experts in the method. This measure is the proportion of all images that contain coral (soft and hard summed). Note that the number of COTS seen has not been incorporated into this calibration (not enough COTS seen in the field trip).
* ReefScan-Deep: as per ReefScan-Transom, except that images were taken using a different measurement platform.
* Coral Transect: performed by a JCU team, experts in the method. Same dive, but different transect, to the SALAD measurements. The measure is the number of points on a transect that lay on coral (soft and hard). The measure of effort is the number of points that lay on hard substrate (approprite habitat).

The details of the model are presented futher below. As are instructions about how to use the pacakge (via illustration). Note that this README is performing a similar role to that of a vignette (so there is no vignette). 

### Installation

The `RosettaCOTS` package can be installed using `devtools` R package.


```r
install.packages('devtools')
devtools::install_github( repo="Scott-Foster/RosettaCOTS")
```

## Funding

This package is an output of the COTS control and Innovation Program (CCIP) program's `Tool Comparison' project (project D-02).

## Contributing Software
Fork the `RosettaCOTS` repository

Clone your fork using the command:

`git clone https://github.com/<username>/RosettaCOTS.git`

Contribute to your forked repository.

Create a pull request.

If your code passes the necessary checks and is documented, your changes 
and/or additions will be merged in the main `RosettaCOTS` repository.

## Reporting Bugs

If you notice an issue with this repository, please report it using [Github Issues](https://github.com/Scott-Foster/RosettaCOTS/issues). When reporting an implementation bug, include a small example that helps to reproduce the error (a non-working minimal example). The issue will be addressed as quickly as possible.

## Seeking Support

If you have questions or need additional support, please open a [Github Issues](https://github.com/Scott-Foster/RosettaCOTS/issues) or send a direct email to scott.foster@data61.csiro.au.


## References 


