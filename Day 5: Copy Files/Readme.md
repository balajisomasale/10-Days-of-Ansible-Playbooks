# This playbook copies a file from the local machine to a target server.
```
---
- name: Copy Files
  hosts: your_target_servers
  tasks:
    - name: Copy Files
      copy:
        src: /path/to/local/file.txt
        dest: /path/on/target/server/file.txt

```

Running Playbook:
make sure you have the file in the Ansible controller to copy it to the target server:

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/ea794a6b-eeb2-436b-9f76-da447d969a09)

Target server:

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/e6431614-b818-47f5-af58-ce3f891941da)
