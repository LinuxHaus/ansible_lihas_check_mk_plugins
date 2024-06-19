# ansible_lihas_check_mk_plugins
Add plugins from check-mk-server

Hopefully something similar will be integrated into the official check-mk ansible collection `checkmk.general`

Please use `checkmk.general` for agent/server setup as such

## Requirements

To run solo:
```
ansible-galaxy install -r requirements.yml
ansible-playbook -i localhost, check_mk.yml
```

## Dependencies

* lihas_variables

## Variables
```
# add/remove check-mk-agent plugins via apt
X.config.check_mk.agent.plugins.[].name: Plugin Name
X.config.check_mk.agent.plugins.[].type:
    * add
    * remove
X.config.check_mk.agent.plugins.[].cache:
    * Cache Time

```

## Example Playbook

```
---
- hosts: '*'
  role: lihas_check_mk_plugins
...
```
