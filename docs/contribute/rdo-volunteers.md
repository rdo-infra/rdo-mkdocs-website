---
title: RDO Volunteers page
---

## Contribute

Do you want to help to resume publishing OpenStack RPMs?

Follow these steps:

1. Join the CentOS Cloud SIG room on Matrix ([#centos-cloud:fedoraproject.org](https://matrix.to/#/#centos-cloud:fedoraproject.org)) and come say hi!
2. Join the [RDO mailing lists](https://www.rdoproject.org/community/mailing-lists/).
3. Create an account on [CentOS community portal](https://accounts.centos.org/).
    - If you already have a Fedora account you can use that too.
4. Create an account on [GitLab.com](https://gitlab.com/users/sign_up).
5. Contact one of the [Cloud SIG sponsors](https://accounts.centos.org/group/sig-cloud/) to join the SIG.
    - This is a manual step required for vetting/spam prevention.
    Do it after introducing yourself to the community.
6. After you are in the Cloud SIG on CentOS accounts system, [link your CentOS account to GitLab](https://sigs.centos.org/guide/auth/#linking-your-centos-account-to-gitlab).
7. Check you are now a [Cloud SIG member on GitLab](https://gitlab.com/groups/CentOS/cloud/-/group_members) too.
8. Read the relevant docs:
    - [Authentication guide](https://docs.centos.org/centos-sig-guide/auth/) - you should be able to install required packages and request a signed TLS certificate.
    - [Build in CBS guide](https://docs.centos.org/centos-sig-guide/cbs/) - you shoud be able to run a `cbs hello` command.
    - [Lookaside cache guide](https://docs.centos.org/centos-sig-guide/git) - complementary to CentOS Build System (CBS) guide.
    - [rdo-volunteers Etherpad](https://etherpad.opendev.org/p/rdo-volunteers) - for a history of what has been done regarding RPM building.
9. Ask the community on Matrix/mailing list how you can help and take part in the periodic meetings.

Do not hesitate to ask for community help in case of issues!

## Status

The RDO Project is being integrated more tightly into CentOS infrastructure:

* Distgit repositories have been migrated in the [Cloud SIG repository on GitLab](https://gitlab.com/CentOS/cloud/rpms).
* CI/CD part is still being discussed.
* Manual builds have been run for some packages on CBS/Koji build.
