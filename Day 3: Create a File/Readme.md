# Create a File
---
- name: Create a File
  hosts: your_target_servers
  tasks:
    - name: Create a File
      file:
        path: /path/to/your/file.txt
        state: touch

Run the playbook:

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/f70693d4-05ce-499a-a89f-9c914c7591a6)

Target server:

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/f2e52aa3-0d2f-4aa6-b0b9-c8a1cfa96086)

------------ what if we want to add line inside a file -------------

You can use the Ansible `lineinfile` module to add or modify lines in a file, including writing an echo message inside a file. Here's an example playbook that demonstrates how to use `lineinfile` to add an echo message to a file:

```
---
- name: Write Echo Message to File
  hosts: your_target_servers
  become: true
  tasks:
    - name: Add Echo Message to File
      lineinfile:
        path: /path/to/your/file.txt
        line: 'echo "Hello, Ansible!" >> /path/to/your/output.txt'
        create: yes  # Create the file if it doesn't exist
```

Explanation:

- `lineinfile`: Ansible module for managing lines in text files.
- `path`: The path to the file where you want to add or modify lines.
- `line`: The line you want to add. In this case, it's an `echo` command that appends "Hello, Ansible!" to another file (`output.txt` in this example).
- `create`: If set to `yes`, Ansible will create the file if it doesn't exist.

Make sure to replace `your_target_servers` with the appropriate group or host in your Ansible inventory, and update the file paths according to your requirements.

Save the playbook in a file, for example, `write_echo.yml`, and run it using the following command:

```
ansible-playbook -i your_inventory_file write_echo.yml
```

This will add the specified echo message to the specified file on your target servers.

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/65d58cd3-f126-4799-8fad-395e33d68dfc)

Target:

![image](https://github.com/balajisomasale/10-Days-of-Ansible-Playbooks/assets/35003840/8d0d62db-9376-45c8-9148-19ee8223f04b)
