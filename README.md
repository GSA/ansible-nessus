nessus [![circleci](https://circleci.com/gh/GSA/ansible-nessus.svg?style=svg)](https://circleci.com/gh/GSA/ansible-nessus)
==================

This ansible role installs and configures the nessus agent required to communicate with client machines.

Requirements
------------

Required Packages (this role requires access to the following packages/installers)
- nessus.rpm - redhat installer package
- nessus.msi - windows installer package

Role Variables
--------------

| Variable | Default | Purpose |
| ------ | ------ | ------ |
| redhat_nessus_agent_filename | "" | redhat installer rpm |
| windows_nessus_agent_filename | "" | windows installer msi |
| nessus_server_id | "" | nessus host |
| nessus_port_id | "" | agent port |
| group_name | "" | nessus agent group name |
| nessus_agent_key | "" | nessus agent key |
| nessus_path | "" | nessus agent path |

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
