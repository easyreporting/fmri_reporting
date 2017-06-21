---
title: "Publishing fMRI results data"
teaching: 15
exercises: 0
questions:
- How can I make my fMRI results publically available?
objectives:
- Learn how to export your results data using NIDM-Results
- Learn how to publish your results data on NeuroVault
keypoints:
- Publishing fMRI results data is a best practice from the statistical literature
- NIDM-Results packs contain images and metadata needed to describe fMRI results 
- NeuroVault is an online repository where those data can be published
---

### Why publishing fMRI results data?
The most widespread approach to analyze task-based fMRI, often termed "mass univariate", is to compute one statistical test at each location in the brain.

Best statistical practices for reporting results of hypothesis tests (e.g. [SAMPL guidelines](http://www.equator-network.org/wp-content/uploads/2013/03/SAMPL-Guidelines-3-13-13.pdf)) call for reporting of the outcome of each test along with a number of statistic including: the p-value, the type of statistic used, the parametrisation of the test statistic (e.g. degrees of freedom for a T-test) and the statistic value. 

For fMRI, complying with theses best practices means publishing one image for each type of statistic to be reported (p-value, statistic value) and a set of metadata describing the testing procedure (type of statistic test, parameters). This lesson describes how to share these data and metadata.

### How can fMRI results data be reused?
Image data describing the the results from multiple fMRI studies can be combined to obtain a quantitative synthesis through image-based meta-analysis. 

<img src="{{site.root}}/fig/NMA.png" width="70%">

### How to publish your fMRI results data?

#### Gathering the data and metadata
All the data and metadat are usually available to the neuroimaging software package that was used to perform the analysis. But each software package has a different way to store these information. The NIDM-Results specification provides a harmonised representation across neuroimaging software packages in the form of a zip archive that contains all the images and metadata describing the results. 


> ## Export your SPM results as a NIDM-Results pack
> ### Install
> The latest version of the NIDM exporter in available in the [last SPM release](http://www.fil.ion.ucl.ac.uk/spm/software/spm12/#Updates).
> ### Usage
> 1. In Matlab, open `SPM`
> 
>    ~~~
>    spm fmri
>    ~~~
>    {: .matlab}
> 1. Open the `Batch Editor` by clicking on the `Batch` button in the SPM12 `Menu` window
> 1. Open the menu `SPM` > `Stats` > `Results Report` (Fig. 1.)
> 3. In the batch window  (Fig. 2.)
>   - Fill in information about the results you are interested in (in particular `SPM.mat` file, contrast number, threshold, etc.)
>   - In `Export results`, selected `New: NIDM (Neuroimaging Data Model)`
>   - Fill in information about your analysis (`Modality`, `Reference space`, `Groups`, etc.) 
>
> More informations at: [https://github.com/incf-nidash/nidmresults-spm](https://github.com/incf-nidash/nidmresults-spm)
{: .challenge}

> ## Export your FSL results as a NIDM-Results pack
> ### Install
> ~~~
> pip install nidmfsl
> ~~~
> {: .shell}
> ### Usage
> ~~~
> nidmfsl [-h] [-g GROUP_NAME NUM_SUBJECTS] [-o OUTPUT_NAME] [-d]
               [-n NIDM_VERSION] [--version]
               feat_dir
> ~~~
> More informations at: [https://github.com/incf-nidash/nidmresults-fsl](https://github.com/incf-nidash/nidmresults-fsl)
{: .challenge}



#### Publication
Results data from fMRI experiments can be shared on [NeuroVault](http://NeuroVault.org). NeuroVault is an online repository that accepts NIDM-Results packs as well as NIfTI images.

> ## Upload your NIDM-Results pack on NeuroVault
> <img src="{{site.root}}/fig/neurovault_upload.png" width="70%">
{: .challenge}


<!-- > ## Callouts
> If you want to introduce a box with a "callout", use this syntax
> This is useful for materials that you think of as explanatory asides
> I usually use this for extra material that is "optional".
{: .callout} -->
