ansible-nessus
=========

Nessus agents are lightweight, low-footprint programs that you install locally on hosts to supplement traditional network-based scanning or to provide visibility into gaps that are missed traditional scanning. This ansible role installs and configures the agent required to communicate with client machines.

Requirements
------------

```bash
redhat_nessus_agent_filename: #redhat installer msi
windows_nessus_agent_filename: #windows installer msi
nessus_server_id: #nessus host
nessus_port_id: #nessus agent port
group_name: #nessus agent group name
nessus_agent_key: #nessus agent key (required)
```

Role Variables
--------------

```bash
None
```

Dependencies
------------
Acquire Installers
```bash
nessus.rpm - redhat installer package
nessus.msi - windows installer package
```

Example Playbook
----------------

```bash
    - hosts: servers
      roles:
         - ansible-nessus
```

License
-------

MIT

Author Information
------------------

Lance White - GSA/GEO
