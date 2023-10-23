# Edge-Image-Automation

## The Why

We need an automated way of creating the artifacts (iso & application) that are required to run Chris on the Edge (ChBox). 



## The What 

The following are required while we are deploying to the Edge 

* Edge Device (Example - Onlogic HX500)
* Blueprint
* Kickstart
* Ansible Automation Platform
* OSTree remote (A remote repository or server that stores OSTree objects, which can include versioned file system trees, binaries, and other content used in the management and deployment of the operating system. OSTree remotes serve as a source from which clients can download and deploy updates or new versions of the file system.)


## The How 

* Run Ansible Playbook via AAP Controller


## References 

* rpm-ostree - https://coreos.github.io/rpm-ostree/
* Ansible and Edge Computing - https://www.redhat.com/en/technologies/management/ansible/edge
