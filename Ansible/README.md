Ansible automates the management of remote systems and controls their desired state.

Components of Ansible:
    1. Control Node:
    2. Managed NOde:
    3. Inventory:
Roles: 
Playbooks:
Plays:
Tasks:
Handlers:
Modules:
Plugins:
Collections:

Working with dynamic inventory
    Ansible supports two ways to connect with external inventory: 1. Inventory plugins and 
                2. inventory scripts.

Master node and worker nodes will connect through:
1. SSH key generation passwordless setup
2. pem file

Working with command line tools Ansible provide:
Ansible galaxy: Command to manage Ansible roles and collections.
Ansible-pull: 
Ansible-vault: encryption/decryption utility for Ansible data files
{create,decrypt,edit,view,encrypt,encrypt_string,rekey}
    create              Create new vault encrypted file
    decrypt             Decrypt vault encrypted file
    edit                Edit vault encrypted file
    view                View vault encrypted file
    encrypt             Encrypt YAML file
    encrypt_string      Encrypt a string
    rekey               Re-key a vault encrypted file
Filters: Data manipulation
Variables concepts:
Tests: tests are used for comparisons
Lookups: Lookup plugins retrieve data from outside sources such as files, databases, key/value stores, APIs, and other services.
Loops: loop, with_<lookup>, and until
Conditionals: 
Blocks: Blocks create logical groups of tasks.
Handlers: Sometimes you want a task to run only when a change is made on a machine.
Error handling in playbooks: 
Roles: Roles let you automatically load related vars, files, tasks, handlers, and other Ansible artifacts based on a known file structure.
Tags: 

Executing playbooks for troubleshooting:
    start-at-task:  ansible-playbook playbook.yml --start-at-task="install packages"
    Step mode:  ansible-playbook playbook.yml --step
Debugging tasks: 

Ansible vault: 

Ansible galaxy: 
