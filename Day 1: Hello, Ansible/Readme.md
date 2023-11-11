# Day 1: Hello Ansible!
Today, we'll start with a simple Ansible playbook to ensure that Ansible is working and can communicate with your servers.
```
---
- name: Hello Ansible
  hosts: your_target_servers
  tasks:
    - name: Print Hello
      debug:
        msg: "Hello, Ansible!"

```
## Run the Ansible Playbook
Navigate to the directory and run the ansible playbook: `ansible-playbook -i inventory playbook.yml`

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/f59238e6-2668-418d-92b3-78569f3bd984)

Note: If you are getting permission denied error, please use `sudo su -` and then creating and running the playbook and it may work!!
