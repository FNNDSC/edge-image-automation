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
### How do install ChRIS in the box ?

* Perform the changes and update version of the Blueprint in the ` edge-device.yaml ` so that the Ansible Automation Platform wil trigger the playbook to generate the iso that can copied from the server manually or remotely.
* Once the ` chris.iso ` file is ready, please use it to boot the device

### I have made some changes , How do I get them on my edge device ?

  * Run the command ` rpm-ostree upgrade `
  * After upgrade is completed , reboot the device using the command` systemctl reboot
  * Verify to ensure the changes are present
    


## References 

* rpm-ostree - https://coreos.github.io/rpm-ostree/
* Ansible and Edge Computing - https://www.redhat.com/en/technologies/management/ansible/edge
