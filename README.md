# Pibasho Builder: The RedBug Household Raspberry Pi Setup

This repo helps you setup a [Raspberry Pi](https://www.raspberrypi.com/) to be a server to provide your household (or other location) with local-first software on your local intranet.

This repository is opinionated, and installs particular things for you. You have some control with configuration, but you might also choose to [fork this repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo) to create one for your own household, and make changes to our setup.

This repository is an example of [Infrastructure as Code](https://en.wikipedia.org/wiki/Infrastructure_as_code) - meaning that your Raspberry Pi server is setup using the code in this repository, rather than by you manually making changes to the Pi yourself. This lets you easily re-build your Pi in case of failure, and still have it working the way you expect.

The particular Infrastructure as Code tool used by this repository is [Ansible](https://www.ansible.com/), and open-source server configuration tool provided by RedHat. While RedHat is a linux company, Ansible works many operating systems, including Windows. However, this repository will use Ubuntu Linux on your Raspberry Pi server, and also most instructions are assuming that Ubuntu Linux is also the operating system on the computer you are using to setup your Pi.

## Prerequisites

### A new Raspberry Pi

* Flash the SD card with Ubuntu Server 64bit.
* Be sure to set a hostname for the PI
* Your ssh key on the pi. Eg: `ssh-copy-id -i ~/.ssh/id_ed25519 pi@radish.local`

### Controlling computer

Your development machine should probably run Linux or these instructions will be wrong.

* Install python3
* Install ansible `pip install ansible`
* Optional: Install `ansible-lint` using `sudo apt install ansible-lint`
* Ensure you have a ssh key created

## Setting Up a New Pi

### Setup hosts file

Copy `hosts-example` in this directory to a new file called `hosts`. Replace the capitalized sections with the correct values for your needs.

### Setup house_vars file

Copy `house_vars_example.yml` in this directory to a new file called `house_vars.yml`. Change any values to suit your house.

### Run the ansible playbook

`ansible-playbook run.yml`

## Maintenance

### Run the playbook again anytime

`ansible-playbook run.yml`

## References

For more details see https://github.com/nginx-proxy/nginx-proxy
