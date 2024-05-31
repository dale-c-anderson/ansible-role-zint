# Ansible role: Zint

![.github/workflows/molecule.yml](https://github.com/AcroMedia/ansible-role-zint/workflows/.github/workflows/molecule.yml/badge.svg)

- Install Zint's build prerequisites
- Build and Install Zint from source on Ubuntu

## Updating Zint

The role does not support updating Zint. To change the installed version of
Zint, first delete `/usr/local/bin/zint`, then install the new version.

## Requirements

* Ubuntu LTS (20.04 or newer)

## Role Variables

If these variables are not supplied, the role will just pull the latest version.

```yaml
zint_version: 2.13.0
zint_source: "https://sourceforge.net/projects/zint/files/zint/{{ zint_version }}/zint-{{ zint_version }}-src.tar.gz/download"
zint_source_checksum: 'sha256:a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1d2e3f4a5b6c7d8'
```

## Dependencies

None

## Example Playbook

```yaml
    # Just download latest
    - hosts: servers
    - roles:
        - name: Install Zint from source
          role: acromedia.zint
      tags:
        - zint

    # ...or download a specific version
    - hosts: servers
    - roles:
        - name: Install Zint from source
          role: acromedia.zint
          zint_version: 2.9.1
          zint_source: "https://sourceforge.net/projects/zint/files/zint/{{ zint_version }}/zint-{{ zint_version }}-src.tar.gz/download"
          zint_source_checksum: 'sha256:bd286d863bc60d65a805ec3e46329c5273a13719724803b0ac02e5b5804c596a'
      tags:
        - zint
```

## License

GPLv3

## Author Information

Acro Commerce Inc.
https://www.acrocommerce.com/
