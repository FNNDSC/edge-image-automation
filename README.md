# Edge-Image-Automation

<img width="1428" alt="Screenshot 2023-10-25 at 2 25 39 PM" src="https://github.com/FNNDSC/edge-image-automation/assets/93591339/2bd547cc-d502-4591-b813-f608d565f289">

## Why

We need an automated way of creating the artifacts (image iso & application) that are required to run Chris in a Box (ChBox). 

## What 

The following are required while we are deploying to the Edge 

* Edge Device (Example - Onlogic HX500)
* Blueprint
* Kickstart
* Ansible Automation Platform
* OSTree remote (A remote repository or server that stores OSTree objects, which can include versioned file system trees, binaries, and other content used in the management and deployment of the operating system. OSTree remotes serve as a source from which clients can download and deploy updates or new versions of the file system.)


## How 
### How do install ChRIS in the box for the first time ?

* Perform the changes and update version of the Blueprint in the ` edge-device.yaml ` so that the Ansible Automation Platform wil trigger the playbook to generate the iso that can copied from the server manually or remotely.
* Once the ` chris.iso ` file is ready to use, please use it (copy to a USB drive)to boot the edge device.
* Chris services will start automatically after the device has been booted. 

### I have made some updates , How do I get them on my edge device ?

  * Run the command ` rpm-ostree upgrade `
  * After upgrade is completed , reboot the device using the command` systemctl reboot
  * Verify to ensure the changes are present
    
### Troubleshooting

To check the pods run `podman pods ps `

To check the status of containers run `podman ps `

To restart chris type ` systemctl restart minichris.service`


## References 

* rpm-ostree - https://coreos.github.io/rpm-ostree/
* Ansible and Edge Computing - https://www.redhat.com/en/technologies/management/ansible/edge
