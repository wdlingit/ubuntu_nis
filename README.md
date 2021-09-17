Role Name
=========

Install a nis master and a set of nis clients. Tested on ubuntu20 xen guests.

Requirements
------------

Specifically written for ubuntu20. May not work for other systems.

Role Variables
--------------

Set master_host as the master and group clients in client_group. Must set subnet_ip, subnet_mask, and master_ip to fit the actual configuration.

Dependencies
------------

None. 

Example Playbook
----------------

    - hosts: all
      become: yes
      roles:
        - role: wdlingit.ubuntu_nis
          master_host: master
          client_group: client_group_defined_in_hosts
          nisdomain: mydomain
          subnet_ip: 10.0.0.0
          subnet_mask: 255.255.255.0
          master_ip: 10.0.0.1

License
-------

MIT
