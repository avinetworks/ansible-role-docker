# avinetworks.docker

[![Build Status](https://travis-ci.org/avinetworks/ansible-role-docker.svg?branch=master)](https://travis-ci.org/avinetworks/ansible-role-docker)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-avinetworks.docker-blue.svg)](https://galaxy.ansible.com/avinetworks/docker/)


This role provides the following:
* Installation of Docker following Docker-Engine install procedures as documented by Docker.
* It will manage kernel versions as well, verifying the that the correct kernel for Docker support is installed.

Supports the following Operating Systems:
* CentOS 6
* CentOS 7
* RedHat 6
* RedHat 7
* Fedora 24
* Fedora 23
* OracleLinux 6
* OracleLinux 7
* Ubuntu 12.04
* Ubuntu 14.04
* Ubuntu 16.04

## Requirements

This role requires Ansible 2.0.0 or higher. Requirements are listed in the metadata file.

## Role Variables

| Variable | Required | Default | Choices | Comments |
|----------|----------|---------|---------|----------|
| `docker_storage_driver` | No | `None` | <ul><li>`devicemapper`</li><li>aufs</li></ul> | The name of the storage driver for docker. |
| `docker_block_device` | No | `None` | <ul><li>`/dev/sda3, etc.`</li></ul> | The device name used for the storage driver. |

## Example Playbook

Install docker to your machine.

    - hosts: servers
      roles:
         - role: avinetworks.docker
           storage_driver: devicemapper
           block_device: /dev/sda3

## License

MIT

## Author Information

Eric Anderson
