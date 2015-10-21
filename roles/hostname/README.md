# Role for hostname configuration<a id="sec-1" name="sec-1"></a>

This role are meant to update the hostname in '/etc/hostname', the IPv4
and the IPv6 aliases in 'etc/hosts'.
The tasks are defined in 'roles/hostname/tasks' folder and the template in
'roles/hostname/templates/'. They use the extra variable {{var\_hostname}} defined
in the inventory file 'hosts'.