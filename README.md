# Mojo Manor Raspberry Pi Setup

## Prerequisites

## A new Raspberry Pi

* Flash the SD card with Raspberry Pi OS Lite
* Be sure to set a hostname for the PI
* Your ssh key on the pi. Eg: `ssh-copy-id -i ~/.ssh/id_ed25519 pi@mojo.local`

## Controlling computer

Your development machine should probably run Linux or these instructions will be wrong.

* Install ansible `sudo apt install ansible`
* Optional: Install `ansible-lint` using `sudo apt install ansible-lint`
* Ensure you have a ssh key created
