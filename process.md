---
layout: page
title: Process
permalink: /process/
---

The [CODE CHECK principles](index) can be implemented in different ways.
On this page [we](team) describe a few alternatives developed during conversations with our [we](team#partners).

In our discussions with editors and publishers, we found that the _point in time_ during the review process when a code check happens, the person who takes the role of codechecker, and the openness of the codechek, can vary.
For example, the check may happen before peer review or after, the codechecker can be staff, a regular reviewer, or a member of a special reproducibility committee, the check may be open or blind, either matching or differing from the scientific review, and the results may be published or confidential.

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQFaeUaBVzc1g39rGRfD9TKJkpC-Je3VY0fd0kClv_EQ-2Xcqr5ZlTYC5SeNtBuLA_UvrLbf_SSQ8Qm/pub?w=770&amp;h=271">

## Post review with extra role

1. A manuscript with computations passes scientific peer-review and is assigned a codechecker with matching expertise (first priority: code, second priority: domain)
1. The codechecker must understand the instructions and executes the workflow using the CODE CHECK infrastructure.
   They contact the manuscript author if needed and collaborate based on the CODE CHECK infrastructure.
1. A CODE CHECK evaluates if the code and data produce a core output (figure, dataset) - it is _not_ a result check or judgement of scientific merit.
1. The codechecker makes the final call on the result within a week, publishes the checked code and data together with the environment in a public repository (with DOI), and puts their name on it. A <img src="/img/codeworks-badge.svg" alt="CODE CHECK badge" height="16" style="margin-top: -4px;" /> badge on the published article points to the repository with the checked files.

### Pre-review by staff

1. An editorial staff member/ECR with technical expertise checks if something is "mechanically wrong" before sending out a submission to review. This is worth the time together with other technical checks! The codechecker can reach out to the author to fix problems.
1. If a code check is successful, start the regular review.
1. After acceptance, add <img src="/img/codeworks-badge.svg" alt="CODE CHECK badge" height="16" style="margin-top: -4px;" /> badge to the published article.

### Parallel reproducibility reviewer

1. ...
