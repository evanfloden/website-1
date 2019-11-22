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
   The priority in all documentation and metadata is that a human codechecker can understand them.
   The codechecker is _not_ making a scientific judgement.
   It is also close to impossible to make a codecheck blind.
   Therefore a CODE CHECK must not be anonymised must provide a two-way means of communication between author and codechecker.
   Codecheckers are supported by formal metadata, automation, and reproducibility infrastructure, yet the check shall not rely on them.
   Codechecks may be conducted by existing stakeholders in the submission process (e.g., a reviewer), but may also be handled with new roles and by people underrepresented in classic peer-review, such as early career resarchers (ECRs) or resarch software engineers (RSEs).
1. <span class="principle">Codecheckers record but don't investigate or fix.</span>
   A codechecker is _not_ required to fix workflows, but to document the given state of documentation and executability.
   Of course, given a level of interested and skills, a codechecker may go beyond simple small fixes and actively collaborate with an authow to create a better research output.
   _Codechecker take the pictures at a crime scene, they do not hunt the murderer._
1. <span class="principle">Credit is given to codecheckers.</span>
   Software and its review are crucial for research in the age of digitisation, so the contribution to the scientific body of knowledge in form of a check gets the credit it deserves, ideally in form of a DOI-able artifact, but at a minimum reporting codechecker (e.g., with ORCID), time, journal/publisher, and (if published) the article DOI.
1. <span class="principle">Workflows are scripted, auditable, and they work.</span>
   Common sense and a collaborative process are the main drivers behind the level of documentation, the degree of openness, and the amount of data that is checked, but the minimal requirement is that the codechecker validates the workflow could be executed once by running a single command.
   Being executed once means that a detailed investigation may occur at a later time.

These basic principles ensure the feasibility of the process in scholarly communication and strike a balance with the ideals of reusable high-quality research software.
Of course, numerous requirements on openness/transparency (e.g. depositing the check result publicly with a DOI), about software quality (tests, releases, documentation), and regarding best practices (e.g. workflow management, data/software citation) are thinkable, but intentionally remain to be defined by implementations of the principles in each community of practice.
While the CODE CHECK initiators strongly support of Open Science, a CODE CHECK does not exclude research not following under your definition of Openness.

### Implementing the CODE CHECK process

_Sketch of steps to implement a CODE CHECK._

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQ02PwUmSs2mCpGh1b9rqI9b6yk8uIVX2RyCj3ac9W2U7quzQHFVJpQtrOxg1eqLrLMD6174PjDfCEq/pub?w=767&amp;h=410">

The above principles can be implemented in different ways.
In our discussions with editors and publishers, we found that the point in time when a code check happens, and the person who takes the role of codechecker can vary.
For example, the check may happen before peer review or after, and the codechecker can be staff, a regular reviewer, or a member of a special reproducibility committee.

_See the [processes page](process) for details about the connection of a code check with a scholarly peer review, and the [technology example](techexample) page for a concrete specification of the practical requirements and steps._

------

To stay in touch with the project follow the [project team](team) members on Twitter:

- [@StephenEglen](https://twitter.com/StephenEglen)
- [@nordholmen](https://twitter.com/nordholmen)
