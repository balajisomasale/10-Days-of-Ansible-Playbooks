```
---
- name: Install and Configure Docker
  hosts: your_target_servers
  become: true
  tasks:
    - name: Install Docker
      yum:
        name: docker
        state: present
    - name: Start Docker
      service:
        name: docker
        state: started
        enabled: true
    - name: Run Nginx Container
      docker_container:
        name: nginx-container
        image: nginx
        ports:
          - "80:80"
```
Tarrget server:
![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/991572f7-3059-49b6-b56e-ed4208ac15ac)
