
```
---
- name: Deploy Web App
  hosts: your_target_servers
  tasks:
    - name: Clone Web App Repository
      git:
        repo: https://github.com/example/web-app.git
        dest: /var/www/web-app
    - name: Start Web App
      command: /var/www/web-app/start.sh


```
