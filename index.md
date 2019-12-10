---
layout: page
---

<img src="img/codecheck_logo.svg" alt="CODE CHECK logo" />

_A process for independent reproduction of computations underlying research_

CODE CHECK tackles one of the main challenges of computational research by supporting codecheckers with a workflow, guidelines and tools to evaluate computer programs underlying scientific papers.
The independent time-stamped runs conducted by codecheckers will award a _"certificate of reproducible computation"_ and increase availability, discovery and reproducibility of crucial artefacts for computational sciences.
See the [project](/project/) page for a full description of problems, solutions, and goals and check out the [GitHub organisation](https://github.com/codecheckers) for code and examples.

### The CODE CHECK principles

1. <span class="principle">Codecheckers are humans and communication is key.</span>
   <details>
   <summary>More about this principle...</summary>
   The priority in all documentation and metadata is that a human codechecker can understand them.
   The codechecker is _not_ making a scientific judgement.
   It is also close to impossible to make a codecheck blind.
   Therefore a CODE CHECK must not be anonymised must provide a two-way means of communication between author and codechecker.
   Codecheckers are supported by formal metadata, automation, and reproducibility infrastructure, yet the check shall not rely on them.
   Codechecks may be conducted by existing stakeholders in the submission process (e.g., a reviewer), but may also be handled with new roles and by people underrepresented in classic peer-review, such as early career resarchers (ECRs) or resarch software engineers (RSEs).
   </details>
1. <span class="principle">Codecheckers record but don't investigate or fix.</span>
   <details>
   <summary>More about this principle...</summary>
   A codechecker is _not_ required to fix workflows, but to document the given state of documentation and executability.
   Of course, given a level of interested and skills, a codechecker may go beyond simple small fixes and actively collaborate with an authow to create a better research output.
   The codechecker's report provides helpful input to the scientific review, e.g., to help the reviewer's understanding.
   But a CODE CHECK does not evaluate scientific merit!
   A failed check does not imply the rejection of a submission.
   <em>Codechecker take the pictures at a crime scene, they do not hunt the murderer.</em>
   </details>
1. <span class="principle">Credit is given to codecheckers.</span>
   <details>
   <summary>More about this principle...</summary>
   Software and its review are crucial for research in the age of digitisation, so the contribution to the scientific body of knowledge in form of a check gets the credit it deserves.
   If a CODE CHECK was conducted as part of a review process, (a) the publisher ensures a proper creditation to the level given to scientific reviewers, e.g. by listen the codechecker on an article or journal page (with number of reviews) or by depositing metadata to public databases (e.g., CrossRef, Publons), and (b) a sentence in the methods section is added mentioning the occured CODE CHECK and the reviewer name.
   The deposited metadata includes a codechecker's ORCID, time, journal, and (if published) the article DOI.
   
   This principle intentionally does not regulate if/how the output of the CODE CHECK is deposited and who does it.
   Ideally though the contribution made by the codechecker is openly published in form of a DOI-able artifact and the sentence in the methods sections links to it as a simple hyperlink/URL.
   </details>
1. <span class="principle">Workflows are scripted, auditable, and they work.</span>
   <details>
   <summary>More about this principle...</summary>
   Common sense and a collaborative process are the main drivers behind the level of documentation, the degree of openness, and the amount of data that is checked, but the minimal requirement is that the codechecker validates the workflow submitted by the authors.
   This means the code could be executed once by running a single command.
   Being executed once means that a detailed investigation may occur at a later time.
   Being auditable includes that authors provide data and code for relevant analsis steps and visualisations to the codecheckers, but does not imply that all of the code associated with an article must be checked.   
   </details>

These basic principles ensure are feasible to add in a scholarly communication process but still have a huge positive impact on the transparency and usefulness of the published material.
They strike a **balance** between the ideals of auditable high-quality research software and the reality of publication pressure and only slowly changing academic evaluation practices.
Of course, numerous requirements on openness/transparency (e.g. depositing the check result publicly with a DOI), about software quality (tests, releases, documentation), on copyright/licensing, and regarding best practices for computer-based analyses (e.g. workflow management, data/software citation) are thinkable, but intentionally remain to be defined by implementations of the principles in each community of practice.
While the CODE CHECK initiators strongly support of Open Science, a CODE CHECK does not exclude research not falling into your definition of Open Science.

**In the future** we hope to update these principles and to work together with researchers, educators, editors, and publishers to raise the bar towards very high reproducibility and openness across all domains and communities of research.

### Implementing the CODE CHECK process

_Sketch of steps to implement a CODE CHECK._

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQ02PwUmSs2mCpGh1b9rqI9b6yk8uIVX2RyCj3ac9W2U7quzQHFVJpQtrOxg1eqLrLMD6174PjDfCEq/pub?w=767&amp;h=410">

The above principles can be implemented in different ways.
In our discussions with editors and publishers, we found that the point in time when a code check happens, and the person who takes the role of codechecker can vary.
For example, the check may happen before peer review or after, and the codechecker can be staff, a regular reviewer, or a member of a special reproducibility committee.

_See the [processes page](process) for details about the connection of a code check with a scholarly peer review, and the [technology example](techexample) page for a concrete specification of the practical requirements and steps._

Stephen Eglen presented CODE CHECK at [The 14th Munin Conference on Scholarly Publishing 2019](http://site.uit.no/muninconf/).
You can take a look at the [poster](https://septentrio.uit.no/index.php/SCS/article/view/4910/4893) and the [slides](https://septentrio.uit.no/index.php/SCS/article/view/4910/4900), or watch the [video recording](https://mediasite.uit.no/Mediasite/Play/8027873496dc465ebc4b9b3ab0338ad01d?playFrom=1772000).

[![](/img/munin-2019.jpg){}](https://mediasite.uit.no/Mediasite/Play/8027873496dc465ebc4b9b3ab0338ad01d?playFrom=1772000)

------

To stay in touch with the project follow the [project team](team) members on Twitter:

- [@StephenEglen](https://twitter.com/StephenEglen)
- [@nordholmen](https://twitter.com/nordholmen)
