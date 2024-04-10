---
title: Infrastructure
---



The following pieces of infrastructure are used during the cycle:

- [review.rdoproject.org](https://review.rdoproject.org) is the central system for our workflow, powered by [SoftwareFactory](https://softwarefactory-project.io/docs/). It contains a Gerrit instance to manage all changes to the repositories where the spec files used to build our packages are contained, as well as the components managing our CI infrastructure.
- [Our distgit repositories](https://github.com/rdo-packages) contain one repository for each project built by RDO, where the spec files are located. Every change submitted via review.rdoproject.org is synchronized to the repos at GitHub.
- [The RDO Trunk repositories](../deliverables/trunk-repos.md) contain the latest packages.
- [The Zuul CI infrastructure](https://review.rdoproject.org/zuul/status) is used to run the periodic jobs to promote the latest repositories.
