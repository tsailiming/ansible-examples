# Introduction
Simple examples for AWS.

# Playbooks
| Filename | Description |
| --------- | ----------- |
| `prov_ec2_apache.yml` | Provisioning N instances with Apache installed |
| `prov_ec2_mariadb.yml` | Provisioning N instances with MariaDB installed |
`start_apache.yml` | Ensure Apache in started and enabled
`stop_apache.yml` | Ensure Apache is stopped
`start_mariadb.yml` | Ensure MariaDB is started and enabled
`stop_mariadb.yml` | Ensure MariaDB is stopped
`patch_apache.yml` | Patch Apache
`patch_mariadb.yml` | Patch MariaDB

# Ansible Tower Integration
The provisioning playbooks can be added to Ansible Tower as job templates, and can be integrated with Tower by defining the `tower_host` and related variables. After provisioning, the new instances and  group defined in the `ec2_server_group_name` variable will be added to the inventory. The inventory  will be created if it does not exists. 

You should **not** change the `ec2_server_group_name` name, otherwise subsequent plays will not run. 

The other playbooks can run from Ansible Tower by using the inventory and will run with the correct host groups such as `apache-hosts` or `mariadb-hosts`.

# Assumptions
The playbooks assume that the instance has Internet connectivity to obtain updates, for example to RHUI.
