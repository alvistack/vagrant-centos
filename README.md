# Vagrant Box Packaging for CentOS

[![GitLab pipeline
status](https://img.shields.io/gitlab/pipeline/alvistack/vagrant-centos/master)](https://gitlab.com/alvistack/vagrant-centos/-/pipelines)
[![GitHub
release](https://img.shields.io/github/release/alvistack/vagrant-centos.svg)](https://github.com/alvistack/vagrant-centos/releases)
[![GitHub
license](https://img.shields.io/github/license/alvistack/vagrant-centos.svg)](https://github.com/alvistack/vagrant-centos/blob/master/LICENSE)
[![Vagrant Box
download](https://img.shields.io/badge/dynamic/json?label=alvistack%2Fcentos-8-stream&query=%24.boxes%5B%3A1%5D.downloads&url=https%3A%2F%2Fapp.vagrantup.com%2Fapi%2Fv1%2Fsearch%3Fq%3Dalvistack%2Fcentos-8-stream)](https://app.vagrantup.com/alvistack/boxes/centos-8-stream)

CentOS (from Community Enterprise Operating System) was a Linux
distribution that provided a free, community-supported computing
platform functionally compatible with its upstream source, Red Hat
Enterprise Linux (RHEL). In January 2014, CentOS announced the official
joining with Red Hat while staying independent from RHEL, under a new
CentOS governing board.

Learn more about CentOS: <https://centos.org/>

## Supported Boxes and Respective Packer Template Links

  - [`alvistack/centos-8-stream`](https://app.vagrantup.com/alvistack/boxes/centos-8-stream)
      - [`packer/libvirt-8-stream/packer.json`](https://github.com/alvistack/vagrant-centos/blob/master/packer/libvirt-8-stream/packer.json)
      - [`packer/virtualbox-8-stream/packer.json`](https://github.com/alvistack/vagrant-centos/blob/master/packer/virtualbox-8-stream/packer.json)
  - [`alvistack/centos-7`](https://app.vagrantup.com/alvistack/boxes/centos-7)
      - [`packer/libvirt-7/packer.json`](https://github.com/alvistack/vagrant-centos/blob/master/packer/libvirt-7/packer.json)
      - [`packer/virtualbox-7/packer.json`](https://github.com/alvistack/vagrant-centos/blob/master/packer/virtualbox-7/packer.json)

## Overview

  - Packaging with [Packer](https://www.packer.io/)
  - Minimal [Vagrant base box
    implementation](https://www.vagrantup.com/docs/boxes/base)
  - Support [QEMU Guest
    Agent](https://wiki.qemu.org/Features/GuestAgent)
  - Support [VirtualBox Guest
    Additions](https://www.virtualbox.org/manual/ch04.html)
  - Support [Vagrant synced folder with
    rsync](https://www.vagrantup.com/docs/synced-folders/rsync)
  - Support [Vagrant provisioner with
    Ansible](https://www.vagrantup.com/docs/provisioning/ansible)
  - Standardize disk partition with GPT
  - Standardize file system mount with UUID
  - Standardize network interface with `eth0`

### Quick Start

Once you have [Vagrant](https://www.vagrantup.com/docs/installation) and
[VirtaulBox](https://www.virtualbox.org/) installed, run the following
commands under your [project
directory](https://learn.hashicorp.com/tutorials/vagrant/getting-started-project-setup?in=vagrant/getting-started):

    # Initialize Vagrant
    vagrant init alvistack/centos-8
    
    # Start the virtual machine
    vagrant up
    
    # SSH into this machine
    vagrant ssh
    
    # Terminate the virtual machine
    vagrant destroy --force

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub
Release](https://github.com/alvistack/vagrant-centos/releases) of this
repository. Thus using these tags will ensure you are running the most
up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab
pipeline](https://gitlab.com/alvistack/vagrant-centos/-/pipelines) in
weekly basis. Thus using these tags will ensure you are running the
latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC
    BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
