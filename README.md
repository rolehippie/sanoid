# sanoid

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/sanoid)
[![General Workflow](https://github.com/rolehippie/sanoid/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/sanoid/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/sanoid/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/sanoid/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/sanoid/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/sanoid/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/sanoid)](https://github.com/rolehippie/sanoid/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/51448)](https://galaxy.ansible.com/rolehippie/sanoid)

Ansible role to install and configure sanoid ZFS backups.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [sanoid_datasets](#sanoid_datasets)
  - [sanoid_templates](#sanoid_templates)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### sanoid_datasets

List of datasets

#### Default value

```YAML
sanoid_datasets: []
```

#### Example usage

```YAML
sanoid_datasets:
  - name: rpool/USERDATA
    use_template: general
    recursive: true
    process_children_only: true
```

### sanoid_templates

List of templates

#### Default value

```YAML
sanoid_templates:
  - name: general
    frequently: 0
    hourly: 24
    daily: 7
    monthly: 12
    yearly: 0
    autosnap: true
    autoprune: true
```

## Discovered Tags

**_sanoid_**

## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
