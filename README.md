kubernetes-master-setup
=======================

This role is created to create Kubernetes Master using kubeadm over aws ec2-instance.

Requirements
------------

There are no requirement. ( Only ansible should be correctly installed and ec2 instance successfully created and inventory entry should be right.)

Role Variables
--------------

Follwing parameters are there :

| Sr.|  PARAMETER | NAME  | USE  | CHANGE PARAMETER AT LOCATION |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|1. |   <b>cidr</b>     (String) ( Required ) | Kubernetes Cluster Network Range  | It denotes Network starting Ip. eg. : 10.240.0.0 | Update it in 'kubernetes-master-node-setup' role defaults/main.yml file or parameters.yml file or   in setup.yml file. | 



Dependencies
------------

There are no dependencies.

Example Playbook
----------------

### To add kubernetes-master-setup Role
```sh
-  hosts: 'kk_master'
    become: yes
    become_method: sudo
    become_user: root
    roles:
          - name: "Master Node Setup"
            role: kubernetes-master-setup

```

### To add kubernetes-master-setup Role ( without previledges)

```sh
-  hosts: 'kk_Master'
    roles:
          - name: "Main Node Setup"
            role: kubernetes-master-setup

```
License
-------

BSD
Free to use.

Author Information
------------------

##### Maintained by: Kaushal Soni
 
### Support & Contact
<b>
Email: Kaushal95300@gmail.com </br>

Linkedin : https://www.linkedin.com/in/kaushal-soni-988650146/ </br>

Github : https://github.com/kush95300 

Medium : https://kaushalsoni.medium.com </b>

 </br>


