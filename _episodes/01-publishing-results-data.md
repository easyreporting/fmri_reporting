---
title: "How to publish fMRI results data?"
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

### Why publishing fMRI results data is a best practice?

In task-based fMRI, we usually perform multiple tests that cover the full brain. Best statistical practices for reporting results of hypothesis tests mandate reporting of the outcome of each test along with the p-value, type of statistic and parameters (e.g. degrees of freedom for a T-test) and the statistic value. For fMRI, this is equivalent with publishing images of brainwise p-values and statistic values along with metadata describing the testing procedure.


### How can fMRI results data be reused?
Image data describing the the results from multiple fMRI studies can be combined to obtain a quantitative synthesis through image-based meta-analysis. 


### Using a template allows to create websites for each of the lectures

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

> ## Exercises and challenges (click on the arrow to the right to open)
>
>  Boxes with "challenges" can be interleaved with the lesson materials.
>  Consider adding a challenge every 15 minutes or so.
>    - This helps participants stay engaged.
>    - It surfaces questions that learners have as they go along.
>    - It breaks up the instruction, providing a bit of a diversion.
>    - It gives people a chance to engage in peer instruction, which is
>      is [known to help learning](https://en.wikipedia.org/wiki/Peer_instruction).
{: .challenge}


> ## Callouts
> If you want to introduce a box with a "callout", use this syntax
> This is useful for materials that you think of as explanatory asides
> I usually use this for extra material that is "optional".
{: .callout}
