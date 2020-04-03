---
layout: page
title: CODECHECK community process guide
permalink: guide/community-process
redirect_from:
  - /techexample/
  - techexample
---

The CODECHECK community process described here is the steps that codecheckers follow when using GitHub, in particular the [GitHub organisation codecheckers](https://github.com/codecheckers/), and Zenodo for codechecking software from scientific articles.
These codechecks may be part of a journal review or not and are a concrete implementation of the abstract [CODECHECK process](/process) following the _[CODECHECK principles](/)_.

## Author responsibilities

The author must provide a [preproducible](doi.org/10.1038/d41586-018-05256-0) workflow: all data and code files necessary to reproduce the results are provided in a way that allows fellow researchers to follow and execute the steps.
Often this workflow includes the generation of key figures from the article based on data.

A typical measure for documentation is to provide at least so much information as the author would themselves need after a long period of time, e.g. 1 year, to run the analysis again.
Any researcher, even if not familiar with the software stack, should be able to run the workflow and find out if the code works.

Common sense shall be applied to decide about the suitable amount of data and to handle big datasets and privacy concerns.
For example, data may be deposited depending on community practices in remote repositories, synthetic data may be used, subsets or preprocessed data may be included, or protected access to information may be provided (e.g. cloud-based data enclaves).

The minimal set of files, besides all required data and code, to implement a CODECHECK process are the following (`/` is the project root directory):

1. **`/README` file** with instructions how to execute the workflow (must be plain text, may have suitable extension, e.g., `.txt`, `.md`, `.markdown`)
1. **`/codecheck.yml` file** with a list of output files created by the workflow, the so called manifest; these files must be created by the workflow and are the basis for validating a successful CODECHECK
1. **`/LICENSE` file** with information about licenses for all submitted material, e.g. code license for scripts and data licenses for used datasets

These files and the worklow are published in a dedicated self-contained _GitHub_ repository in the [codecheckers organisation](https://github.com/codecheckers/).
After the CODECHECK, authors may use a pull request to transfer the improvements and certificate back to their own repository.

Beyond that, any additional configuration and information is extremely helpful, of course.
Concrete guidelines as to what this can entail are given by the codechecker's tasks below and the concept of a [research compendium](https://research-compendium.science/).

## Codechecker tasks

The codechecker in general is not there to fix things, but to document how far they go and give feedback to the author until a CODECHECK could be completed or is found impossible (see _[principle 2](/)_).
However, a codechecker may, for example out of personal interest in the research at hand, invest additional efforts.
In any case, the overall goal is to _leave the workflow repository in the same or better condition_.

Prerequisite: familiarity with `make`, https://the-turing-way.netlify.com/make/make.html & https://swcarpentry.github.io/make-novice/reference.

- [Open an issue on the CODECHECK register](https://github.com/codecheckers/register/issues) to notify other codecheckers.
- Fork the repository to the codecheckers GitHub organisation, or create a new repository (following the terms and conditions of the workspace licenses)
- Create a directory `codecheck` to not interfere with original files (may use `.codecheck` if `codecheck` exists in submission).
  All files that are by no chance created by an author go into this directory.
  Other files that an author could have used must not be hidden in this CODECHECK-related directory, but just be added to the appropriate location (see "leave in a better condition" above).
- Re-run the workflow based on provided documentation, i.e. recreate all files listed in the manifest, based on a `Makefile`
  - template found at XXXX
  - Create a notebook?
- Document the used computing environment, see [CODECHECK bundle guide](/guide/bundle).
- Add a _CODECHEK report_ file **`codecheck.pdf`**
  - WHO checked WHAT, and HOW?
  - template for CODECHEK report at XXXX
  - Optional CODECHEK report content depending on interest, time, and skills:
    - Do the generated outputs match the ones in the original manuscript? Are the differences relevant or not?
    - Are used pieces of software and data properly CITED and publicly DEPOSITED und suitable LICENSES?
    - Are open formats (text-based) included?
    - Is data and [software](https://content.iospress.com/articles/data-science/ds190026) FAIR?
- Add all codechecker-contributed information to the **`codecheck.yml`** file, see [spec](/spec/config/latest)
- Deposit the CODECHEK report on _Zenodo_ under you name, adding the original authors as co-authors
  - preregister a DOI on Zenodo
  - add the DOI to the `codecheck.yml` file
  - add the DOI to the `codecheck.pdf` CODECHEK report
  - You can add any material to this record that you see fit, especially things that helped you with your reproduction, i.e. the [CODECHECK bundle](/guide/bundle)
  - Add the record to the [CODECHECK community on Zenodo](https://zenodo.org/communities/codecheck)
- Add the CODECHECK to the register. If the check was conducted for the first time for a piece of software or resulted in important lessons learned, consider adding it to the list of examples below.
- Add the [CODE WORKS badge](https://github.com/codecheckers/website/tree/master/badges) to the article or the original software repository. The badge should link directly to the Zenodo record <img src="/img/codeworks-badge.svg" alt="CODECHECK badge" height="16" style="margin-top: -4px;" />
- Update the register issue with all important information, then close it.

Every CODECHECK is unique, just as the associated research article.
The codechecker can thereby rely on the examples below and future published CODECHECKs for good practices and approaches for codechecking.

## Start a CODECHECK

[Open a new issue](https://github.com/codecheckers/register/issues/new/choose) on the CODECHECK register with information about your workflow.

## Examples

See the [CODECHECK register on GitHub](https://github.com/codecheckers/register/) for a full list of codechecks.

### [Piccolo, 2020](https://github.com/codecheckers/Piccolo-2020)

Codechecker: [@sje30](https://github.com/sje30)

Report: [http://doi.org/10.5281/zenodo.3674056](http://doi.org/10.5281/zenodo.3674056)

Journal: GigaScience

### [Hopfield, 1982](https://github.com/codecheckers/Hopfield-1982)

A landmark paper from neuroscience, reproduced by [@sebwyh](https://github.com/sebwyh) with edits by [@nuest](https://github.com/nuest).

Codechecker: [@nuest](https://github.com/nuest)

Comments:

- seed not set, but human can judge the code works
- codechecker added `requirements.txt` using `pip freeze` after workflow could be executed
- codechecker added text to README about the computing environment

### Eglen, 2015 (work in progress)

https://github.com/codecheckers/eglen2015/

Draft CODECHECK report: https://github.com/sje30/codecheck/blob/master/cert/eglen2016/eglen2016-crc.Rmd

### Hancock, 1991 (work in progress)

https://github.com/codecheckers/Reproduction-Hancock

### Hathway Goodman, 2018 (work in progress)

https://github.com/codecheckers/Hathway-Goodman-2018

### Detorakis, 2017 (work in progress)

https://github.com/codecheckers/Detorakis-reproduction

### Larisch, 2019 (work in progress)

https://github.com/codecheckers/Larisch-reproduction

### Barto Sutten Anderson, 1983 (work in progress)

https://github.com/codecheckers/Barto-Sutton-Anderson-1983
