# Playbook<a id="sec-1" name="sec-1"></a>

This playbook is meant to build an entire infrastructure stack with
frameworks on which i'm currently working.
This playbook is tested on Debian 8.4 Jessie, so I recommend to use that to test these modules.

This stack can be on a single node or multiples nodes. You can manage them in the inventory
file ``hosts``.

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


To define your own user account, please take a look at [users role](roles/users/vars/main.yml)
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
