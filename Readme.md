## Brief

* Create a hosted git repository account of your choice (if you do not already possess one) e.g. github, gitlab, bitbucket, etc.
* Provide us with the account name
* Create a public repository for this assessment and provide the name once complete
* Use the repository for the configuration and code that will:
   * Spin up a Linux Vagrant box of your choice
   * Configure Vagrant to use Ansible as the provisioner
   * Configure the box with an IP address available to the hosting OS
   * Write playbook/playbooks to:
     * Install and start docker
     * Build a docker container based on the official Alpine Linux container (library/alpine:latest)
     * Build the container so that nginx is installed and started
     * Configure nginx to serve out some static “Hello World” content
     * Start the container as a micro service
* Write appropriate documentation in the repository to explain how someone cloning it should provision the Vagrant VM and access the web URL serving out the “Hello World”

## Success Criteria:
   * The web page should be available from the hosting OS - localhost:8080

## Requirements
  * Vagrant 2.0 or higher
  * Ansible 2.4 or higher

## Installation/Provisioning
  One simple command will create the vagrant box, install docker on the guest OS, create the docker container and install Nginx
  That magical command is - 
```
vagrant up
```