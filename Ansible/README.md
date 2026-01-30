# Ansible Kubespray


vms.yaml = basic vm's configuration

start:

```
ansible -i inventory/inventory.yaml all -m ping -K
ansible -i /inventory/inventory.yaml vms.yaml -K 

# COnfigure VM's
ansible-playbook -i inventory/hosts.yml playbook.yml -K
```



## Kubespray with Ansible


- Clone the main kubespray repo with ansible playbooks and roles

- Do the steps to install kubespray



## Fix ip drift on control plane

kubeadm reset && kubeadm init
