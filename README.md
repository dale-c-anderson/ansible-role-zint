# Ansible role: Zint

- Install Zint's build prerequisites
- Build and Install Zint from source on Ubuntu

## Requirements

* Ubuntu LTS (14.04 or newer)

## Role Variables

See example playbook.

## Dependencies

None

## Example Playbook

    - hosts: servers
    - roles:
        - name: Install Zint from source
          role: acromedia.zint
          zint_version: 2.4.2
          zint_source: "https://github.com/downloads/zint/zint/zint-{{ zint_version }}.tar.gz"
          zint_source_checksum: 'sha256:76547faaba0bfbea43733ab324e498863ebf21fc9a2e5db93512739d661a2b3a'
      tags:
        - zint

## License

GPLv3

## Author Information

Acro Media Inc.
https://www.acromedia.com/
