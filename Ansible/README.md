# Ansible Overview

Ansible is an open-source automation tool that helps streamline and manage IT infrastructure, software deployment, and workflow orchestration via YAML-based playbooks

<br>

# Ansible Playbooks

* `---` Marks the beginning of a document (Optional) 
* `...` Marks the end of a document (Optional) 
* Indentation is crucial (Use spaces instead of tabs)

<br>

```YAML
---
- name: PLAYBOOK_NAME
  hosts: 
  vars:
    key: value
  tasks:
    - name: TASK_NAME
    apt:
...   
```

| Ansible Playbook Parameter | Description |
| --- | --- |
| `name` | |
| `hosts` | | 
| `vars` | | 
| `tasks` | | 

<br>