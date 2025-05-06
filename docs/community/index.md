# Community

Help us make the RDO community site a great place for users and cloud operators in the Red Hat ecosystem. There are many ways to contribute to RDO, some of which are detailed below.

Our community strives to operate according to the terms of the
[OpenStack Code of Conduct](https://www.openstack.org/legal/community-code-of-conduct/).

If you're just getting started, and are looking for a little help,
consult our [mentors list](../contribute/mentors.html.md).


## People person

* [Join the RDO mailing lists](mailing-lists.md)
* Chat on #rdo on OFTC
* [Participate in weekly meetings](community-meeting.md)

## Latest RDO activity

### RDO Epoxy 2025.1 released!

RDO Epoxy 2025.1 Release - Important Note at Bottom

The RDO community is pleased to announce the general availability of RDO builds for OpenStack 2025.1 Epoxy for RPM-based distributions, CentOS Stream and Red Hat Enterprise Linux. RDO is suitable for building private, public and hybrid clouds. Epoxy is the 31st release of the OpenStack project, backed by over 1,000 contributors worldwide.

This release is already available on CentOS Stream 9 on the CentOS mirror network:

https://mirror.stream.centos.org/SIGs/9-stream/cloud/x86_64/openstack-epoxy/

The RDO community project curates, packages, builds, tests, and maintains a complete set of OpenStack components for RHEL and CentOS Stream and is a member of the CentOS Cloud SIG. The Cloud SIG focuses on delivering a great user experience for CentOS users looking to build and maintain on-premise, public, or hybrid clouds.

All work on RDO and its downstream release, Red Hat OpenStack Services on OpenShift, is 100% open source, with all code changes going into it's related upstream first.

You can read the broader upstream OpenStack project highlights at https://releases.openstack.org/epoxy/highlights.html, but here are some highlights:

Notably, active/active support for Dell PowerStore, Dell PowerStore QoS support, NetApp adding support for active/active mode in ISCSI/FC drivers, HPE Nimble replication, and StorPool adding support for pool-to-pool cloning.
To address OSSN-0090 and OSSN-0065, support was added for a new add/get location API that replaces the image update (old location-add) mechanism for consumers such as cinder and nova.
Ironic includes multiple security improvements:
All supported mechanism drivers (ML2/OVS, ML2/OVN) can now use the WSGI API module, and the first phase of deprecation of the eventlet library is complete.
Instances with UEFI can now boot in stateless pending if the image has the hw_firmware_statelessproperty and the compute service has libvirt 8.6.0 or later.


According to this model (https://governance.openstack.org/tc/resolutions/20220210-release-cadence-adjustment.html), upgrades will only be supported from the Caracal 2024.1 release to the next SLURP release (phase Epoxy).

RDO Epoxy 202 5.1 has been published by the CentOS Storage SIG in the official CentOS repository and has been built and tested with the latest released Ceph 18.2.0 Reef version (https://docs.ceph.com/en/latest/releases/reef/). *Note:* Follow the instructions in the [RDO documentation](https://www.rdoproject.org/install/install-with-ceph/) to install OpenStack and Ceph services on the same host.


During Epoxy cycle, some projects have been retired or declared inactive upstream. As such, the following packages for some projects are not present in the RDO Epoxy 2025.1 release:

python-saharaclient (https://review.rdoproject.org/r/c/rdoinfo/+/54360)
puppet-corosync (https://review.rdoproject.org/r/c/rdoinfo/+/53127)
python-oauth2client (dependency https://review.rdoproject.org/r/c/rdoinfo/+/54115)

During the next release we will continue working on retiring inactive packages in order to ensure RDO content quality and security. 

Contributors:
During the Epoxy cycle, we saw the following new RDO contributors:

Ashish Gupta
Dmitriy Chubinidze
Francisco Seruca Salgado
Ivan Anfimov
Lilach Avraham
Manoj Katari
Saurabh Agarwal
Sofer Athlan-Guyot
Viji Candappa

Welcome to all of you and Thank You So Much for participating!

But we wouldn’t want to overlook anyone. A super massive Thank You to all 51 contributors who participated in producing this release. This list includes commits to rdo-packages, rdo-infra, and rdo-website repositories:

Alan Pevec
Alfredo Moralejo
Amy Marrich
Ananya Banerjee
Artom Lifshitz
Ashish Gupta
Bogdan Dobrelya
Chandan Kumar
Daniel Pawlik
Dmitriy Chubinidze
Douglas Viroel
Eduardo Olivares
Fiorella Yanac
Francesco Pantano
Francisco Seruca Salgado
Harald Jensås
Ivan Anfimov
Jakub Libosvar
Jaromír Wysoglad
Joan Francesc Gilabert
Joel Capitao
Karolina Kula
Lewis Denny
Lilach Avraham
Luigi Toscano
Manoj Katari
Maor Blaustein
Martin Kopec
Matthias Runge
Matthieu Huin
Miguel Garcia
Mikołaj Ciecierski
Pablo Rodríguez Nava
Pooja Jadhav
Rabi Mishra
Radomir Dopieralski
Rodolfo Alonso
Ronelle Landy
Saurabh Agarwal
Sergii Golovatiuk
Shreshtha Joshi
Sławek Kapłoński
Sofer Athlan-Guyot
Takashi Kajinami
Tobias Urdin
Tony Breeds
Viji Candappa
Yatin Karel


The Next Release Cycle
At the end of one release, focus shifts immediately to the next release i.e Epoxy.

Get Started

To spin up a proof of concept cloud, quickly, and on limited hardware, try an All-In-One Packstack installation. You can run RDO on a single node to get a feel for how it works.

For those that do not have any hardware or physical resources, there is the OpenStack Global Passport Program. This is a collaborative effort between OpenStack public cloud providers to let you experience the freedom, performance and interoperability of open source infrastructure. You can quickly and easily gain access to OpenStack infrastructure via trial programs from participating OpenStack public cloud providers around the world.

Get Help
The RDO Project has our users@lists.rdoproject.org for RDO-specific users and operators. For more developer-oriented content we recommend joining the dev@lists.rdoproject.org mailing list. Remember to post a brief introduction about yourself and your RDO story. The mailing lists archives are all available at https://www.rdoproject.org/community/mailing-lists/. You can also find extensive documentation on RDOproject.org.

The #rdo channel on OFTC IRC is also an excellent place to find and give help.

We also welcome comments and requests on the CentOS devel mailing list and the CentOS IRC channels (#centos, #centos-cloud, #centos-devel in Libera.Chat network), however we have a more focused audience within the RDO venues.

Join us in #rdo and on the OFTC IRC network. You can also find us on Facebook and YouTube. 

Important Note!
We had a thriving, if small, group of community members maintaining packages prior to COVID and we need to return to those days of having folks participate in this effort. The OpenStack RPM packaging effort is in need of package maintainers in order to continue having RPMs. The current maintainers have moved on to new opportunities, so while we have folks continuing to contribute, we currently have no folks to build and maintain packages. Please check out the RDO contribute pages, peruse the CentOS Cloud SIG page, and inhale the RDO packaging documentation. Please reach out if you can help!

### Centos Connect, Brussels, 2024


<iframe width="630" src="https://www.youtube.com/embed/LocoEPmbL4U" title="OpenStack RDO deployment on Community Distribution of Kubernetes (OKD)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Centos Connect, Brussels, 2023


<iframe width="630" src="https://www.youtube.com/embed/jaoIph_mEqM" title="From code to cloud - the journey of Openstack package" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

See more at dedicated [page](rdo-videos.md).


## User

* Share questions and solutions on [openstack mailing lists](https://lists.openstack.org/mailman3/lists/)
* Add [the most useful solutions](../misc/troubleshoot.md)


## Discuss


### IRC channels

Come chat in real-time with RDO users on **IRC** on the [OFTC](http://oftc.net) server:

* **#rdo**: Any general conversation about RDO, including developer issues and user questions. ([Transcripts.](http://eavesdrop.openstack.org/irclogs/%23rdo/))

* **#openstack**: Remember that RDO is just a small part of a larger community. Questions about OpenStack in general, not specifically about RDO, should go to the upstream channel. ([Transcripts.](http://eavesdrop.openstack.org/irclogs/%23openstack/))


Come chat in real-time with the CentOS Cloud SIG  on **IRC** on the [Libera Chat](http://libera.chat) server:

* **#centos-cloud**: If you have questions about the CentOS [Cloud Special Interest Group (SIG)](https://sigs.centos.org/cloud/) and the parts of the RDO infrastructure that run in the CentOS Community Build System (cbs), this is where you're most likely to get answers.
* **#centos-devel**: If you have questions about the CentOS Project

### IRC meetings

We have weekly IRC meetings you can participate in:

* [RDO meetings @ every Wednesday at 14:00 UTC on #rdo on OFTC](community-meeting.md)
* [CentOS Cloud SIG meetings on the second Thursday of the month at 15:00 UTC on #centos-meeting on Libera Chat](https://sigs.centos.org/cloud/communication/meetings/)


## Content writer

All contributions are welcome, so if you would like to contribute to this page or propose change, there are two options for that:

* [Propose change by Gerrrit](https://review.rdoproject.org/r/q/project:rdo-infra%252Frdo-mkdocs-website)
* [Create RDO Jira issue](https://issues.redhat.com/projects/RDO/issues) (selecting "documentation" component during creation), if you are not familiar with this workflow, however, you can find instructions in our [onboarding](https://www.rdoproject.org/contribute/onboarding/).



## Additional sources

- Check our [Frequently Asked Questions (FAQ) page](faq.md) for answers to common questions
- Try our [troubleshooting page](../misc/troubleshoot.md) for solutions to common problems
- Watch [RDO videos](rdo-videos.md). These include recorded talks and community events.
- Help improve our knowledge base by turning the best answers to questions on the [mailing lists](mailing-lists.md).
- [Fork the website on Github](https://github.com/redhat-openstack/website) and help us improve our documentation.
