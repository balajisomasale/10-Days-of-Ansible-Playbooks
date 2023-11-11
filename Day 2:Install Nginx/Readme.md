# Day 2: Install Nginx
On day two, we'll create a playbook to install Nginx on your servers. 
This is a common task and a great way to get started with package management in Ansible.

```
---
- name: Install Nginx
  hosts: your_target_servers
  become: true
  tasks:
    - name: Install Nginx
      yum:
        name: nginx
        state: present
    - name: Start Nginx
      service:
        name: nginx
        state: started
        enabled: true
```

Running the Playbook: `ansible-playbook -i inventory playbook.yml`

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/f154fb2f-5d32-4a3d-8e85-8aa6e96c45b7)

Checking Target server:
- check the nginx version:
  ![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/4406b345-d0d5-4d59-8b92-ea0100b25a30)
- check its status: `systemctl status nginx`
  ![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/1573f883-52fc-4583-ad74-6c6b63d47f2e)
