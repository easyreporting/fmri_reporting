---
title: "Publishing fMRI results data"
teaching: 15
exercises: 0
questions:
- "Why publishing fMRI results data?"
objectives:
- TODO
- TODO
keypoints:
- TODO
- TODO
---

### Why publishing fMRI results data
The most widespread approach to analyze task-based fMRI, often termed "mass univariate", is to compute one statistical test at each location in the brain.

Best statistical practices for reporting results of hypothesis tests (e.g. [SAMPL guidelines](http://www.equator-network.org/wp-content/uploads/2013/03/SAMPL-Guidelines-3-13-13.pdf)) call for reporting of the outcome of each test along with a number of statistic including: the p-value, the type of statistic used, the parametrisation of the test statistic (e.g. degrees of freedom for a T-test) and the statistic value. 

For fMRI, complying with best practices means publishing one image for each type of statistic to be reported (p-value, statistic value) and a set of metadata describing the testing procedure (type of statistic test, parameters). This lesson describes how to share these data and metadata.

### How can fMRI results data be reused?
Image data describing the the results from multiple fMRI studies can be combined to obtain a quantitative synthesis through image-based meta-analysis. 

### How to publish your fMRI results data

#### Gathering the data and metadata
All the data and metadat are usually available to the neuroimaging software package that was used to perform the analysis. But each software package has a different way to store these information. The NIDM-Results specification provides a harmonised representation across neuroimaging software packages in the form of a zip archive that contains all the images and metadata describing the results. 


> ## Export your SPM results into a NIDM-Results pack
>
>  Boxes with "challenges" can be interleaved with the lesson materials.
>  Consider adding a challenge every 15 minutes or so.
>    - This helps participants stay engaged.
>    - It surfaces questions that learners have as they go along.
>    - It breaks up the instruction, providing a bit of a diversion.
>    - It gives people a chance to engage in peer instruction, which is
>      is [known to help learning](https://en.wikipedia.org/wiki/Peer_instruction).
{: .challenge}

> ## Export your FSL results into a NIDM-Results pack
>
>  Boxes with "challenges" can be interleaved with the lesson materials.
>  Consider adding a challenge every 15 minutes or so.
>    - This helps participants stay engaged.
>    - It surfaces questions that learners have as they go along.
>    - It breaks up the instruction, providing a bit of a diversion.
>    - It gives people a chance to engage in peer instruction, which is
>      is [known to help learning](https://en.wikipedia.org/wiki/Peer_instruction).
{: .challenge}



#### Publication

To enable access to the materials in an open format, but allow different
instructors freedom in constructing their own materials, we provide a template
(you're looking at it!), that can be relatively easily adapted to create lesson
materials for many different lessons

To create a new lesson out of the template

### Template lesson files are markdown files

* They are in the `_episodes` folder.
* They are named sequentially:
  - `01-first-part.md`
  - `02-second-part.md`
  - etc


### Markdown format allows you to create nice web-pages

And with only a really small amount of effort! It's text based, so you can
write exactly what you intend to say.

If you want to introduce a block of code into your lesson, write a block
fenced by triple-tilde. Here is an example of that

~~~
import nibabel as nib
img = nib.load('my_file.nii.gz')
affine = img.affine
~~~
{: .python}


Images can be embedded into the lesson plan, by using the following syntax:

![an image]({{site.root}}/fig/fmri_reporting_logo.png)

To embed images, you will also want to copy the image file into the
`fig` folder of the repository, and add that.



> ## Callouts
> If you want to introduce a box with a "callout", use this syntax
> This is useful for materials that you think of as explanatory asides
> I usually use this for extra material that is "optional".
{: .callout}
