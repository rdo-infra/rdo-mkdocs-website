---
title: Install
---

# RDO OpenStack deployment

There have always been multiple ways of deploying OpenStack. In RDO we are using some of them.


## Packstack

For an initial test deployment, follow the [Packstack](./packstack.md) instructions. While using Packstack is sufficient as a proof of concept, there are other ways that you can
use to deploy OpenStack with RDO.


## Puppet OpenStack Integration

This is a collection of scripts and manifests for module testing. During the promotion process, we can continuously test and validate OpenStack setups deployed with Puppet modules. More about can be found in official [documentation](https://docs.openstack.org/puppet-openstack-guide/latest/) and in the [repository](https://github.com/openstack/puppet-openstack-integration).


## OpenStack Ansible

[This project](https://github.com/openstack/openstack-ansible) has partial support for RDO as provider for binary installations in CentOS, hovewer it's not tested in our CI. Main documentation can be find [here](https://docs.openstack.org/openstack-ansible/latest/), there is also available a [deployment guide](https://docs.openstack.org/project-deploy-guide/openstack-ansible/latest/).


## RDO on OKD - experimental

Deployment of OpenStack based on [OKD, The Community Distribution of Kubernetes](https://www.okd.io/), where OpenStack management is handled through a new podified control plane (a set of tools for deploying and managing an OpenStack control plane as Kubernetes-native pods). You can read documentation and instructions about [RDO on OKD Proof of Concept](https://sigs.centos.org/cloud/rdo_on_okd/introduction/), which is a part of [CentOS CloudSIG](https://sigs.centos.org/cloud/). Also you can watch [RDO's presentation](../community/rdo-videos.md#centos-connect-brussels-2024) which is explaining that concept in details.


## TripleO

If you need to deploy a production-ready cloud with an **OpenStack Zed or earlier** release, possibly with HA, see the [TripleO quickstart](./tripleo.md).


## Tools used in RDO

* [DLRN: What it is, what we use it for](../factory/dlrn.md)
* [SoftwareFactory](https://softwarefactory-project.io/)
