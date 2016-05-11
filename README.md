# Playbook<a id="sec-1" name="sec-1"></a>

This playbook is meant to build an entire infrastructure stack with
frameworks on which i'm currently working.
This playbook is tested on Debian 8.4 Jessie, so I recommend to use that to test these modules.

This stack can be on a single node or multiples nodes. You can manage them in the inventory
file ``hosts``.

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
    
    [marathon]
    host3 ansible_ssh_user=username
    host4 ansible_ssh_user=username
    host5 ansible_ssh_user=username


To define your own user account, please take a look at [this folder](roles/users/vars/main.yml)
and copy your own public key in [this folder](roles/users/files)

## Roles :<a id="sec-1-2" name="sec-1-2"></a>

Here is the roles available :
-   Hostname - Configuration
-   Users - Creation and configuration
-   Sudoers - Configuration
-   Apache Mesos - Configuration and installation
-   Apache Zookeeper - Configuration and installation
-   Docker - Configuration and installation
-   Marathon framework - Configuration and installation
-   Mesos-DNS server

# TODO :<a id="sec-2" name="sec-2"></a>

-   Apache Aurora
-   More coming...
