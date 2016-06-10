# Ansible Role: Skel

[![Build Status](https://travis-ci.org/AttestationLegale/ansible-role-skel.svg?branch=master)](https://travis-ci.org/AttestationLegale/ansible-role-skel) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-skel-blue.svg)](https://galaxy.ansible.com/AttestationLegale/skel/)

Manage unix `skeleton`.

## Requirements

None

## Role Variables

For a complete list of variables, see `default/main.yml`.

    skel_default_owner: 'root'
    skel_default_group: 'root'
    skel_default_directory_mode: '0750'
    skel_default_file_mode: '0640'

    skel_default_link_force: False
    skel_default_link_mode: '0640'
    skel_default_link_state: 'link'

    skel_entries: []
    skel_group_entries: []
    skel_host_entries: []

## Dependencies

None

## Example Playbook

```yaml
---
  - hosts: all
    roles:
      - skel
    vars:
      skel_entries:
        - path: /etc/skel/.ssh
          state: directory
```

## License

MIT / BSD

## Author Information

This role was created in 2016 by [ALG](https://www.attestationlegale.fr)
