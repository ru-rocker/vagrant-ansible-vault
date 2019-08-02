# Overview
Playbook example for getting remote host credentials from `hashicorp vault`

# Workspace Parts

#### Hashicorp Vault
Assume the vault already up and running on `https://127.0.0.1:8200`

#### Vagrantfile
Two remote hosts with IP Address `172.20.20.100` and `172.20.20.101`

#### Ansible Playbook
The playbook will retrieve credentials from vault the create user in remote machines.
We will user TLS mechanism to connect to vault.

# Important note
Because this playbook using username and password to connect to machine, instead of 
`ssh-copy-id` mechanism, we need to install `sshpass` first.

Additional variables to be exported for make this playbook run, due to self-signed certificate and sshpass:

       export ANSIBLE_HOST_KEY_CHECKING=False
       export VAULT_SKIP_VERIFY=true


