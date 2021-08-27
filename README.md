Ansible role for MacOS Notarization Client
========================

Ansible role to install MacOS Notarization Client

[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-macos-notarization-client/workflows/Molecule%20Test/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-macos-notarization-client/actions?query=workflow%3A%22Molecule+Test%22)
[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-macos-notarization-client/workflows/Release/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-macos-notarization-client/actions?query=workflow%3A%22Release%22)

Requirements
------------

None

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
| `mac_notarization_client_url` | The url for the curator binary | string | `https://macos-notary-1628249594.s3.amazonaws.com/releases/client/{{ mac_notarization_client_sha }}/macnotary.tgz` | no |
| `mac_notarization_client_sha` | The sha for the curator binary | string | `5621db79b05e5929ca4abd4159d39f9ab8b1ad20` | yes |

Dependencies
------------

None

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
        - role: ansible-role-macos-notarization-client
          vars:
            curator_sha: 5621db79b05e5929ca4abd4159d39f9ab8b1ad20
```

License
-------

[Apache License](LICENSE)
