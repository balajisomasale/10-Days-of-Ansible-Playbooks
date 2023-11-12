# This playbook displays distribution facts for each target server.

```
---
- name: Set System Facts
  hosts: your_target_servers
  tasks:
    - name: Display System Facts
      debug:
        var: ansible_facts['distribution']
```

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/2cee986d-e17a-43a8-bbec-831c43aa0e41)

