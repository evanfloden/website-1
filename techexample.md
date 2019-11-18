---
layout: page
title: CODE CHECK technical example
permalink: /techexample/
---

## Author responsibilities

The author must provide a [preproducible](doi.org/10.1038/d41586-018-05256-0) workflow: all data and code files necessary to reproduce the results are provided in a way that allows fellow researchers to follow and execute the steps.
Often this workflow includes the generation of key figures from the article based on data.

A typical measure for documentation is to provide at least so much information as the author would themselves need after a long period of time, e.g. 1 year, to run the analysis again.
Any researcher, even if not familiar with the software stack, should be able to run the workflow and find out if the code works.

Common sense shall be applied to decide about the suitable amount of data and to handle big datasets and privacy concerns.
For example, data may be deposited depending on community practices in remote repositories, synthetic data may be used, subsets or preprocessed data may be included, or protected access to information may be provided (e.g. cloud-based data enclaves).

The minimal set of files, besides data and code, to implement a CODE CHECK process are the following:

1. **`README` file** with instructions how to execute the workflow
1. **`MANIFEST` file** with a list of output files created by the workflow - these must be created by the workflow and are the basis for validating a successful check
1. **`LICENSE` file** with information about licenses for all submitted material, e.g. code license for scripts and data licenses for used datasets

These files and the worklow are published in a dedicated self-contained _GitHub_ repository.

Beyond that, any additional configuration and information is extremely helpful, of course.
Concrete guidelines as to what this can entail are given by the codechecker's tasks below and the concept of a [research compendium](https://research-compendium.science/).

## Codechecker tasks

Prerequisite: familiarity with `make`, https://the-turing-way.netlify.com/make/make.html

- Create a directory `codecheck` to not interfere with original files (may use `.codecheck` if `codecheck` exists in submission)
- Re-run the workflow based on provided documentation, i.e. recreate all files listed in `MANIFEST`, based on a `Makefile`
  - template found at XXXX
  - Create a notebook?
- Document the used computing environment using suitable configuration files, see [_REES_ specification](https://repo2docker.readthedocs.io/en/latest/config_files.html#config-files), for example by creating one or several of the following files or tools:
  - `Dockerfile`
  - Binder
  - `environment.yml`
  - `requirements.txt`
  - `DESCRIPTION` file (R package)
- Add a _report_
  - WHO checked WHAT, and HOW?
  - Are used pieces of software and data properly CITED and publicly DEPOSITED und suitable LICENSES?
  - Are open formats (text-based) included?
  - Is data and [software](https://content.iospress.com/articles/data-science/ds190026) FAIR?
  - template found at XXXX
- Deposit the original material along with the reproduced files on _Zenodo_ under you name, adding the original authors as co-authors

Every code check is unique, just as the associated research article.
The codechecker can thereby rely on the following examples and future published code checks for good practices and approaches.

## Overview

## Examples

### [Hopfield, 1982](https://github.com/codecheckers/Hopfield-1982)

A landmark paper from neuroscience, reproduced by [@sebwyh](https://github.com/sebwyh) with edits by [@nuest](https://github.com/nuest).

Codechecker: [@nuest](https://github.com/nuest)

Comments:

- seed not set, but human can judge the code works
- codechecker added `requirements.txt` using `pip freeze` after workflow could be executed
- codechecker added text to README about the computing environment

### Hancock, 1991

TBD

### 

TBD

### 

TBD


## FAQ

### Why `make` ?

<!-- make on Windows? -->

- it's old, works, and is available
- caching

### How should I best package my code and data?

So that the codechecker can make sense of it.
Beyond that, follow community practices or create a [research compendium](https://research-compendium.science/).

### What if I used proprietary software _X_?

The codechecker must be able to conduct the check.
If they have access to he software, there is no problem.

### Can't researchers cheat by just creating the `MANIFEST` files?

Yes.

### But I work with huge/privacy data!

- enclaves
- synthetic data
- subsets

### Why does a research have to provide licensing information?

In this first implementation of the CODE CHECK principles described here, we imagine an Open process, and there is no Openness without proper handling of copyright.

### Why don't you require containers?

The codechecker put's their name under the check.
That is more important than technical details, which will vary on a case by case basis.

### What if Docker/`make`/software _X_ is not available anymore?

Software stacks are volatile, and CODE CHECK acknowledges this by focussing on the idea that a workflow was _once_ reproducible by a person other than the author.
This is a _huge_ step forward, and we are excited for the times when even more will be commonplace.
The check largely increases the chances that the checked code works for third parties and is accessible, e.g. using text-based file formats, and portable, e.g. using containers.
The _files_ and _archives_ (a Docker image is a tarball of a directory system) will be readable much longer than tools will be there to easily work with them.
