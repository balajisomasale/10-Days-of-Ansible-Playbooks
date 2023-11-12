# This playbook installs and starts the MySQL server.
```
---
- name: Install and Configure MySQL
  hosts: your_target_servers
  become: true
  tasks:
    - name: Install MySQL
      yum:
        name: mysql-server
        state: present
    - name: Start MySQL
      service:
        name: mysqld
        state: started
        enabled: true
```

