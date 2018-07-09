# Abstract
This is an example of using Ansible Tower Workflow to provision VM on Red Hat Virtualization.

# Workflow

![workflow](pics/Screen Shot 2018-07-09 at 4.21.03 PM.png?raw=true)


![Survey form](pics/Screen Shot 2018-07-09 at 4.46.50 PM.png?raw=true)

# Playbooks
The workflow runs the following Playbooks:
* `prov.yml`: This will provision a single VM on RHV
* `register.yml`: This will register the VM with Red Hat Satellite using 1) activation key 3) Apply Updates 3) Configure OpenSCAP client
* `oscap_scan.yml`: Runs `foreman_scap_client` scan against the Policy ID
* `harden.yml`: Harden the VM using CIS Ansible Role
* `tower.yml`: Add the new IP to Tower inventory
