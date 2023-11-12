# Configure Firewall Rules
```
---
- name: Configure Firewall
  hosts: your_target_servers
  become: true
  tasks:
    - name: Allow HTTP
      firewalld:
        service: http
        permanent: true
        state: enabled
    - name: Reload Firewall
      firewalld:
        state: reloaded
```

