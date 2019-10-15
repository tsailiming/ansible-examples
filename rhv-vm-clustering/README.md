Dependencies
---

This will install the [ansible.ha-cluster-pacemaker](https://github.com/tsailiming/ansible.ha-cluster-pacemaker) role.
```
# ansible-galaxy install -r requirements.yml

```

Sample inventory
---

`vm_name` must be the name in RHV Manager.

```
[servers]
192.168.0.169 vm_name=cluster1
192.168.0.170 vm_name=cluster2
```

Running the playbook
---
```
# ansible-playbook -i hosts cluster.yml
```