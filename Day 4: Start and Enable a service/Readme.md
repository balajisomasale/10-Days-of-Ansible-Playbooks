# This playbook starts and enables a service.
```
---
- name: Start and Enable Service
  hosts: your_target_servers
  become: true
  tasks:
    - name: Start and Enable Service
      service:
        name: your_service_name
        state: started
        enabled: true

```
Prometheus is running in Target server: It is Active

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/52cd702b-5381-4082-85ef-d1a6023686cf)

Running Playbook:
```
---
- name: Start and Enable Service
  hosts: your_target_servers
  become: true
  tasks:
    - name: Start and Enable Service
      service:
        name: prometheus
        state: stopped
        enabled: False
```

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/36b7d8aa-8d5d-473e-86d3-8f8d6f705a69)

Post run in Target: It is Inactive

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/c42e283e-f65f-4ed8-8844-d1be099c63c7)
