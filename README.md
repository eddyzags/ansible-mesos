# Playbook

Those playbooks and roles are meant to build an entire infrastructure stack with
frameworks on which i'm currently working. (tested on Debian 8.4 Jessie)
You can manage your target server(s) in the inventory file ``production``.

PLEASE MAKE SURE THAT YOUR CONFIGURATIONS ARE ALL WELL-DEFINED IN THE
APPROPRIATE ROLES FOLDERS.

    [all]
    host1
    host2
    host3
    host4
    host5
    
    [zookeeper]
    host1 zoo_id=1
    host2 zoo_id=2
    host3 zoo_id=3
    
    [mesos-master]
    host1
    host2
    host3
    
    [marathon]
    host3
    host4
    host5


To define your own user account, take a look at [users role](roles/users/vars/main.yml)___
and copy your own public key in [this folder](roles/users/files)

## Roles

Here is the roles available :
-   Hostname - Configuration
-   Users - Configuration
-   Sudoers - Configuration and packages
-   Apache Mesos - Configuration and packages
-   Apache Zookeeper - Configuration and packages
-   Docker - Configuration and packages
-   Marathon framework - Configuration and packages
-   Mesos-DNS server - Configuration and packages

# TODO

-   Apache Aurora
-   More coming...
