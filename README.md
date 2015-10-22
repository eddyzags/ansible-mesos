# Ansible - My Playbook

Ansible is a simple way to automate apps and IT infrastructure
(Configuration and deployment). It is both humanm-readable and
machine-parsable through playbooks.

## Building my infrastructure stack and deploying application using Ansible playbook

Required : Ansible 1.7.2

This playbook are meant to build an entire infrastructure stack with
applications on which i'm currently working. All you need is ip addresses and root
passwords of the remote hosts. This playbook is tested on Debian 8.1 Jessie,
so I recommend to use that to test these modules.

This stack can be on a single node or multiples nodes. You can add
or remove them on the inventory file 'hosts'.

    [all]
    host1 var_hostname=node1
    host2 var_hostname=node2
    host3 var_hostname=node3
    
    [dbservers]
    host4 var_hostname=node1-db
    host5 var_hostname=node2-db

If you use it, I recommend you to change the
'roles/users/vars/main.yml' to set your user credential and put your
public key in 'roles/users/files/'. The name's file must be the
same as the one you put in the 'ssh\_key' subelement in 'roles/users/vars/main.yml'.

## Roles :

Here is the roles available :
-   hostname configuration
-   users creation and configuration
-   sudoers configuration
-   Apache Mesos
-   Apache Zookeeper
-   Marathon framework

# TODO :

-   Advanced Packaging Tool configuration
-   Apache Aurora (Mesos framework : Scheduler)
-   More coming...