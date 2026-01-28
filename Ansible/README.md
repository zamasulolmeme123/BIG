# Ansible Kubespray


vms.yaml = basic vm's configuration

start:

```
ansible -i inventory/inventory.yaml all -m ping -K
ansible -i /inventory/inventory.yaml vms.yaml -K 

# COnfigure VM's
ansible-playbook -i inventory/hosts.yml playbook.yml -K
```

