# Open Data Policies Decoded Ansible Playbooks

## Summary

These playbooks are meant only to provision a server to host a copy of the Open
Data Policies Decoded website. Because Open Data Policies Decoded is
essentially an instance of [StateDecoded](https://github.com/statedecoded/
statedecoded), this playbook should also be useable for provisioning a server
to host an instance of the State Decoded website.

## Introduction

Everything should largely follow the [Ansible best practices directory layout]
(http://docs.ansible.com/ansible/playbooks_best_practices.html#directory-
layout), with the exception that all of the inventories are under the
`inventories` directory.

The `inventories/group_vars` directory should also have example files detailing
which variables it expects to have populated. Simply copy or rename the
appropriate example inventory and group variable files, then populate them with
the necessary values before use.

The actual deployment of website builds is handled by a separate continuous
delivery/deployment solution, so these playbooks do not cover deploying the
website itself.

The primary playbook to run is `site.yml` at the root directory of the
repository, and you can configure which Ansible roles will be used from that
file.
