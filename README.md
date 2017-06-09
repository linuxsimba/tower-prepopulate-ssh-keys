# Prepopulate SSH Host Keys

Playbook that prepopulates SSH host keys into tower nodes using ``ssh-keyscan``.

## Requirements

* Ansible Tower 3.0+


## Prequisites

* Add this playbook as a Ansible Tower Project
* Give the awx user on the Tower nodes to access to login

## Execution

```
# tower_vars.yml

ssh_proxy: True
ssh_proxy_ip: 10.1.1.1
ssh_proxy_user: jumphost

tower_hosts:
  - towernode1
  - towernode2

tower_user: awx


```

Run this playbook as a Tower Job Template. Run the ``known_host.yml`` playbook in the job template

## License
MIT


