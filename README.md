# Ansible vSphere

First start by updating your variables in `group_vars/all.yml`.

For security reasons you should encrypt your variable file.
```
ansible-vault encrypt group_vars/all.yml
```
Then run:
```
ansible-playbook playbook.yml -- ask-vault-pass
```
This is the file structure:
```
.
├── ansible.cfg
├── group_vars
│  └── all.yml
├── inventory.ini
├── playbook.yml
└── roles
   ├── commons
   │  ├── defaults
   │  │  └── main.yml
   │  └── tasks
   │     └── main.yml
   ├── ctop
   │  └── tasks
   │     └── main.yml
   ├── docker
   │  ├── handlers
   │  │  └── main.yml
   │  └── tasks
   │     └── main.yml
   ├── ssh-config
   │  ├── handlers
   │  │  └── main.yml
   │  └── tasks
   │     └── main.yml
   ├── ssh-port
   │  ├── handlers
   │  │  └── main.yml
   │  ├── tasks
   │  │  ├── main.yml
   │  │  └── user.yml
   │  └── vars
   │     └── main.yml
   ├── user
   │  ├── tasks
   │  │  └── main.yml
   │  └── vars
   │     └── main.yml
   └── vmware
      ├── tasks
      │  └── main.yml
      └── vars
         └── main.yml
```
