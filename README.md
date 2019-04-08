# DevOps_code_challenge
Small code challenge for DevOps/Infra Engineering practices.

# Goal
Deploy a highly-available service and the automation sscripts requried to provision and scale it.

# Task
Using Ansible you need to deploy 2 instances of an Nginx container and balance external calls through HAProxy.
The calls must *only* be served on port 80. Successfully reaching an nginx container must disaply the following message:
```
Hello! This is <hostname>
```
NOTE: Hostname can be the actual hostname of the VM on which the container resides or the name of the container.

# Acceptance Criteria
* This repository must be forked
* The base on which you will be installing all software and moving parts must be comprised of at least one VM running a Linux Distribution of your choice. We are using CentOS for our internal purposes but any LINUX distro is acceptable.
* You will use Vagrant and VBox to support the VMs (or anything similar)
* The provided Dockerfile is used as a base to complete the challenge.
* Composing the custom message displayed by Nginx is done automatically through a script.
* Everything is kept/done in code and provisioning is done through Ansible (where applicable)
* Add a new section to the README for:
	* Providing instructions on how to deploy your setup
	* Providing a breakdown of any roles and variables used in Ansible

When you are done, you will provide us access to your fork.

# Extra Points
Not going the extra mile will not weigh negatively on the evluation of this challenge. But we highly value anyone that is willing to go that extra mile.
* Create a self-healing mechanism for any of the three services involved. Anything that gets the job done is acceptable. (HINT: We use SystemD)
* Containerise HAProxy as well.
* Make your set-up fully scalable. When creating your code, you always have to option to cater it to the given situation, but going the extra mile to make everything agnostic and re-usable will help you and your collegues on the long run.

# Questions
#### What scripting language can I use?
You can use anything that you like but be prepared to justify your decision. We use a combination of Bash, Python and Groovy scripts internally.
#### What if the provided requirements above are not clear or incomplete?
Please feel free to contact us along the way for any inquiries about confusing bits, unclear requirements or if you feel anything is just plain missing.
#### Why does this challenge not include ... ?
I'm glad you asked! We're more than happy to hear about improvements you think might be helpful in making this challenge better.
