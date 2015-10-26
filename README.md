# Ansible - My Playbook

Ansible is a simple way to automate apps and IT infrastructure
(Configuration and deployment). It is both humanm-readable and
machine-parsable through playbooks.

## Building my infrastructure stack and deploying application using Ansible playbook

Required : Ansible 1.7.2

This playbook are meant to build an entire infrastructure stack with
applications on which i'm currently working. All you need is the ip
addresses, the users login and the sudo rights enable for these users
of the remote hosts (NOPASSWD). This playbook is tested on Debian 8.1
Jessie, so I recommend to use that to test these modules.

This stack can be on a single node or multiples nodes. You can add
or remove them on the inventory file 'hosts'.

PLEASE MAKE SURE THAT YOUR CONFIGURATIONS ARE ALL WELL-DEFINED IN THE
APPROPRIATE ROLES FOLDERS.

    [all]
    host1 var_hostname=node1
    host2 var_hostname=node2
    host3 var_hostname=node3
    host4 var_hostname=node4
    host5 var_hostname=node5
    
    [zookeeper]
    host1 zoo_id=1
    host2 zoo_id=2
    host3 zoo_id=3
    
    [mesos-master]
    host1 ansible_ssh_user=username
    host2 ansible_ssh_user=username
    host3 ansible_ssh_user=username
    
    [mesos-slave]
    host1 ansible_ssh_user=username
    host2 ansible_ssh_user=username
    host3 ansible_ssh_user=username
    host4 ansible_ssh_user=username
    host5 ansible_ssh_user=username
    
    [marathon]
    host3 ansible_ssh_user=username
    host4 ansible_ssh_user=username
    host5 ansible_ssh_user=username

If you use it, I recommend you to change the
'roles/users/vars/main.yml' to set your user credential and put your
public key in 'roles/users/files/'. The name's file must be the
same as the one you put in the 'ssh\_key' subelement in 'roles/users/vars/main.yml'.

## Roles :

Here is the roles available :
-   hostname configuration
-   users creation and configuration
-   sudoers configuration
-   Advanced Packaging Tool configuration
-   Apache Mesos
-   Apache Zookeeper
-   Docker configuration and installation
-   Marathon framework

# TODO :

-   Apache Aurora (Mesos framework : Scheduler)
-   More coming...