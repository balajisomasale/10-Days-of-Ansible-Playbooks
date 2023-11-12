# This playbook creates and then deletes users on target servers.

```
---
- name: Create and Delete Users
  hosts: your_target_servers
  become: true
  tasks:
    - name: Create Users
      user:
        name: "{{ item }}"
        state: present
      with_items:
        - user1
        - user2
    - name: Delete Users
      user:
        name: "{{ item }}"
        state: absent
      with_items:
        - user1
        - user2

```

Target server:

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/62ad7b8c-18aa-4bc8-8b62-b583910bd25e)
