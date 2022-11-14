OPNsense: General
=================

An Ansible role to configure basic system settings on opnSense firewalls.

Requirements
------------

This role requires the `lxml` python package to be installed on the host system.

Role Variables
--------------

|            Variable            |  Type  |             Description             |
| :----------------------------: | :----: | :---------------------------------: |
|   opnsense_general_hostname    | string | The hostname to set for the system. |
|    opnsense_general_domain     | string |  The domain to set for the system.  |
| opnsense_general_search_domain | string |   The search domain to configure.   |
|   opnsense_general_timezone    | string | The timezone to set for the system. |
|  opnsense_general_dns_server   | string | The IP address for the DNS server.  |
|   opnsense_general_language    | string |         The language code.          |

Dependencies
------------

N/A.

Example Playbook
----------------

```yaml
- name: Configure all firewalls
  hosts: opnsense

  roles:
    - role: mirceanton.opnsense_general
      vars:
        opnsense_general_hostname: homebase
        opnsense_general_domain: local
        opnsense_general_search_domain: local
        opnsense_general_timezone: Europe/Bucharest
        opnsense_general_language: en_US
        opnsense_general_dns_server: "1.1.1.1"
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
