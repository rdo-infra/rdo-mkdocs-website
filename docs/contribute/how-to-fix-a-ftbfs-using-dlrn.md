---
author: Frederic Lepied
title: How to fix a FTBFS using DLRN
---

DLRN is the tool used by the RDO project to build RPM packages for every commit from the OpenStack projects. See [article](../factory/dlrn.md) for more details on how DLRN works. These commits from the upstream OpenStack projects can introduce changes that break the packaging. We call these FTBFS (Failure To Build From Source).
When we have a FTBFS reported by DLRN, someone needs to take care of fixing it. You can see these using gerrit at [https://review.rdoproject.org/#/q/topic:rdo-FTBFS.](https://review.rdoproject.org/#/q/topic:rdo-FTBFS.)
We’ll work on an example reported on the horizon package in [https://review.rdoproject.org/r/#/c/1131/1/.](https://review.rdoproject.org/#/q/topic:rdo-FTBFS.) Here are the steps to propose a correction:
```
First you need to install DLRN:
git clone [https://github.com/openstack-packages/DLRN.git](https://github.com/openstack-packages/DLRN.git)
cd DLRN
tox
. .tox/py27/bin/activate
```

Then let DLRN build the horizon project to be sure we reproduce the build issue locally:
dlrn --config projects.ini --package-name horizon --dev --head-only

Keep in mind that the default projects.ini file will try to create a package for the master branch using CentOS7 as a target. If the failure happens in a different branch, such as stable/mitaka, you will need to adjust the file as needed.
The dist-git repository is stored under data/_distro so extract the gerrit review in this directory:
```
cd data/horizon_distro
git review -s
git review -d 1131
```
Edit the spec file to fix the problem. Remember to remove the last line in the spec file, it was created by the dummy review. Here in this case, we just needed to remove files not distributed anymore and then archive the change in git resetting the author to take the ownership of the review:
```
git commit --amend -a --reset-author
cd ../..
```
To test your change use the same build command as before with the addition of –local to use your modifications:
```
dlrn --config projects.ini --package-name horizon --dev --head-only --local
```
If everything is fine, just submit the change using the rdo-FTBFS topic:
```
cd data/horizon_distro
git review -t rdo-FTBFS
```
Then you’ll need to have the review accepted by a core reviewer. In our example, here is the proposed changeset to fix the problem: [https://review.rdoproject.org/r/#/c/1131/2/](https://review.rdoproject.org/#/q/topic:rdo-FTBFS.)
