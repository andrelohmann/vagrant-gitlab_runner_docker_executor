# VAGRANT gitlab_runner_docker

(c) Andre Lohmann (and others) 2020

## Maintainer Contact
 * Andre Lohmann
   <lohmann.andre (at) gmail (dot) com>

## content

This repo offers a Vagrant Template to set up a gitlab runner with docker executor running inside a vagrant (virtualbox) machine on a developer machine.

The vagrant machine is based on ubuntu 18.04 installing docker and gitlab-runner. The dependencies are installed using the vagrant ansible_local provisioner.

## prequesites (developer machine)

  * virtualbox
  * vagrant

## Usage

Clone the repo, jump into the cloned directory and configure to your needs

### Configuration

  * Copy **vagrant.config.yml.example** to **vagrant.config.yml**
  * Customize memory and cpus to your needs and available resources
  * Copy **ansible_vagrant/custom_vars.yml.example** to **ansible_vagrant/custom_vars.yml**
  * Customize the following variables:
    * **gitlab_runner_description** - the description your runner will be given
    * **gitlab_external_url** - the gitlab url your runner should talk to
    * **gitlab_runner_token** - the registration token
    * **gitlab_runner_tags** - a list of tags your runner should use

### Run

```
vagrant up
```
