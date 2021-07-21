# Ansible role: Zint

![.github/workflows/molecule.yml](https://github.com/AcroMedia/ansible-role-zint/workflows/.github/workflows/molecule.yml/badge.svg)

- Install Zint's build prerequisites
- Build and Install Zint from source on Ubuntu

## Requirements

* Ubuntu LTS (20.04 or newer)

## Role Variables

See example playbook.

## Dependencies

None

## Example Playbook

    - hosts: servers
    - roles:
        - name: Install Zint from source
          role: acromedia.zint
          zint_version: 2.9.1
          zint_source: "https://sourceforge.net/projects/zint/files/zint/{{ zint_version }}/zint-{{ zint_version }}-src.tar.gz/download"
          zint_source_checksum: 'sha256:bd286d863bc60d65a805ec3e46329c5273a13719724803b0ac02e5b5804c596a'
      tags:
        - zint

## License

GPLv3

## Author Information

Acro Media Inc.
https://www.acromedia.com/
