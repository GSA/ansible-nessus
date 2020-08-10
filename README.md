nessus [![circleci](https://circleci.com/gh/GSA/ansible-nessus.svg?style=svg)](https://circleci.com/gh/GSA/ansible-nessus)
==================

This ansible role installs and configures the nessus agent required to communicate with client machines.

Requirements
------------

Required Packages (this role requires access to the following packages/installers via an external repository)
- nessus.rpm - redhat installer package
- nessus.msi - windows installer package

Role Variables
--------------

### Universal

| Variable | Default | Purpose |
| ------ | ------ | ------ |
| nessus_server_id | "" | nessus host |
| nessus_port_id | "" | agent port |
| nessus_agent_key | "" | nessus agent key |

### Windows

| Variable | Default | Purpose |
| ------ | ------ | ------ |
| windows_nessus_agent_path | "C:\\Program Files\\Tenable\\Nessus Agent" | default windows install directory |
| windows_nessus_agent_url | "" | windows installer msi |
| windows_nessus_product_id | "" | windows product_id |
| windows_agent_log | "C:\Temp\Logs" | default agent windows log directory |

### Redhat

| Variable | Default | Purpose |
| ------ | ------ | ------ |
| redhat_nessus_agent_path | "/opt/nessus_agent/sbin/nessuscli" | default redhat install directory |
| redhat_nessus_agent_url | "" | redhat installer rpm |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - nessus
```

Public domain
-------------

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
