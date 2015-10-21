# Role for users configuration

This role are meant to create and configure the users on the remote hosts
machines. If you want to add more users or your user crendential,
modify the 'roles/users/vars/main.yml' file following this model :

-   username : eddy.zagabe  (Required)
    name : Eddy Zagabe (Required)
    uid : 1001 (Required)
    ssh\_keys :
    -   eddy-zagabe.keys (Required : This is the public key located in 'roles/users/files/eddy-zagabe.keys')

Several extra variables are defined in the 'roles/users/defaults/main.yml'
file. Don't hesitate to open it up to find more information about the
configuration.