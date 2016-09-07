# rav-ipfabric-demo

Ansible project to configure an IP Fabric on Ravello.  

This project is leveraging some custom Ansible roles to dynamically create this topology on ravello.

# Installation

Create a local copy of the project
```
git clone https://github.com/dgarros/rav-ipfabric-demo.git
```

Install Ansible and Juniper.junos roles for ansible
```
TODO
```

Install the Ansible roles for Ravello [instructions](http://ravello-ansible.readthedocs.io/en/latest/install.html)


# How to use

Create application
```
ansible-playbook pb.rav.create.yaml --forks=1
```

Start all VMs
```
ansible-playbook pb.rav.deploy.yaml --forks=1
```

Collect public IP and save locally
```
ansible-playbook pb.rav.get_fqdn.yaml
```

_wait 5 minutes_
Generate configuration and deploy
```
ansible-playbook pb.conf.all.commit.yaml
```
