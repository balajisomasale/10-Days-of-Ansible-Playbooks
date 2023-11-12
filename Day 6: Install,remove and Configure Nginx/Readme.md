# This playbook installs and starts the Nginx web server.

To remove exisitng Nginx: `yum remove nginx-agent`
```
---
- name: Install and Configure Nginx
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
