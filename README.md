# Ansible Role: Atom

[![Build Status](https://travis-ci.org/tonyapuzzo/ansible-role-atom.svg?branch=master)](https://travis-ci.org/tonyapuzzo/ansible-role-atom)

An Ansible Role that installs [Atom](https://www.atom.io) on Linux.

There are 19 (Crazy!) repositories with this name in GitHub already, but none of them actually configure the repositories so that Atom is kept up to date after installation with via `apt ugrade` or `yum update`.  This is fine if you are using Ansible once but if you are using Ansible to create a development environment that might live a few months then it's not great.  Hence I created this one to build a longer-term viable Atom installation.

As an adherent of the Unix Philosophy of doing one thing at a time, this role doesn't manage Atom packages.  See [jgkim/ansible-role-atom](https://github.com/jgkim/ansible-role-atom) for a role that installs packages.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    atom_package: atom
    atom_package_state: present

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - tonyapuzzo.atom
```

## License

MIT / BSD

## Author Information

This role was created in 2018 by Tony Apuzzo as a derivative of [ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker) by [Jeff Geerling](https://www.jeffgeerling.com/).
