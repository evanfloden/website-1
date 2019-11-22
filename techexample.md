---
layout: page
title: CODE CHECK default process
permalink: /techexample/
---

This page documents the _default_ concrete implementation of a [CODE CHECK process](/process) developed by the [CODE CHECK core team](/team).
See the _[CODE CHECK process](/process)_ page for alternative approaches and the _[principles](/)_ for the foundations of a CODE CHECK.

## Author responsibilities

The author must provide a [preproducible](doi.org/10.1038/d41586-018-05256-0) workflow: all data and code files necessary to reproduce the results are provided in a way that allows fellow researchers to follow and execute the steps.
Often this workflow includes the generation of key figures from the article based on data.

A typical measure for documentation is to provide at least so much information as the author would themselves need after a long period of time, e.g. 1 year, to run the analysis again.
Any researcher, even if not familiar with the software stack, should be able to run the workflow and find out if the code works.

Common sense shall be applied to decide about the suitable amount of data and to handle big datasets and privacy concerns.
For example, data may be deposited depending on community practices in remote repositories, synthetic data may be used, subsets or preprocessed data may be included, or protected access to information may be provided (e.g. cloud-based data enclaves).

The minimal set of files, besides all required data and code, to implement a CODE CHECK process are the following (`/` is the project root directory):

1. **`/README` file** with instructions how to execute the workflow (must be plain text, may have suitable extension, e.g., `.txt`, `.md`, `.markdown`)
1. **`/MANIFEST` file** with a list of output files created by the workflow - these must be created by the workflow and are the basis for validating a successful check
1. **`/LICENSE` file** with information about licenses for all submitted material, e.g. code license for scripts and data licenses for used datasets

These files and the worklow are published in a dedicated self-contained _GitHub_ repository in the [codecheckers organisation](https://github.com/codecheckers/).
After the check, authors may use a pull request to transfer the improvements and certificate back to their own repository.

Beyond that, any additional configuration and information is extremely helpful, of course.
Concrete guidelines as to what this can entail are given by the codechecker's tasks below and the concept of a [research compendium](https://research-compendium.science/).

## Codechecker tasks

The codechecker in general is not there to fix things, but to document how far they go and give feedback to the author until a check could be completed or is found impossible (see _[principle 2](/)_).
However, a codechecker may, for example out of personal interest in the research at hand, invest additional efforts.
In any case, the overall goal is to _leave the workflow repository in the same or better condition_.

Prerequisite: familiarity with `make`, https://the-turing-way.netlify.com/make/make.html & https://swcarpentry.github.io/make-novice/reference.

- Fork the repository to the codecheckers org
- Create a directory `codecheck` to not interfere with original files (may use `.codecheck` if `codecheck` exists in submission).
  All files that are by no chance created by an author go into this directory.
  Other files that an author could have used must not be hidden in this check-related directory, but just be added to the appropriate location (see "leave in a better condition" above).
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
  - template for report at XXXX
  - Optional report content depending on interest, time, and skills:
    - Do the generated outputs match the ones in the original manuscript? Are the differences relevant or not?
    - Are used pieces of software and data properly CITED and publicly DEPOSITED und suitable LICENSES?
    - Are open formats (text-based) included?
    - Is data and [software](https://content.iospress.com/articles/data-science/ds190026) FAIR?
- Deposit the original material along with the reproduced files on _Zenodo_ under you name, adding the original authors as co-authors

Every code check is unique, just as the associated research article.
The codechecker can thereby rely on the following examples and future published code checks for good practices and approaches.

## Examples

### [Hopfield, 1982](https://github.com/codecheckers/Hopfield-1982)

A landmark paper from neuroscience, reproduced by [@sebwyh](https://github.com/sebwyh) with edits by [@nuest](https://github.com/nuest).

Codechecker: [@nuest](https://github.com/nuest)

Comments:

- seed not set, but human can judge the code works
- codechecker added `requirements.txt` using `pip freeze` after workflow could be executed
- codechecker added text to README about the computing environment

### Eglen, 2015

https://github.com/codecheckers/eglen2015/

Draft check report: https://github.com/sje30/codecheck/blob/master/cert/eglen2016/eglen2016-crc.Rmd

### Hancock, 1991

https://github.com/codecheckers/Reproduction-Hancock

### Hathway Goodman, 2018

https://github.com/codecheckers/Hathway-Goodman-2018

### Detorakis, 2017

https://github.com/codecheckers/Detorakis-reproduction

### Larisch, 2019

https://github.com/codecheckers/Larisch-reproduction

### Barto Sutten Anderson, 1983

https://github.com/codecheckers/Barto-Sutton-Anderson-1983

------

## FAQ

### Are the CODE CHECK principles not a quite low bar?

Yes.

- A little bit is more than nothing.
- The lower the bar, the earlier in the process a CODE CHECK can occure (e.g. pre-review)
- Exposure to reproducibility practices is key.
- Nudging works.
- Better get a certificate for small parts of the workflow than not doing any code checks - not everything needs to be checked.

### Why `make` ?

<!-- make on Windows? -->
- It's old, works, and is available everywhere.
- Use the caching mechanism.

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
