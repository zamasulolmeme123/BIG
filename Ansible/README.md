# Ansible Kubespray


vms.yaml = basic vm's configuration

start:

```
ansible -i /inventory/inventory.yaml vms.yaml -k PASS 
```