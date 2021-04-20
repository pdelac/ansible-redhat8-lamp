# ansible-redhat8-lamp
Ansible Playbook to create LAMP in Redhat 8 with Apache, MySQL, PHP.
-------------------------------------------

This playbook require Ansible 2.3.2.0.

This playbook has been tested on Redhat 8.x.

1. MySQL is replaced with MariaDB - We use MySQL Community Version

This LAMP stack can be on a single node or multiple nodes. The inventory file
'hosts' defines the nodes in which the stacks should be configured.

        [webservers]
        ipaddress

        [dbservers]
        ipaddress

You can create Digital Ocean droplets and use their IP addresses.
Make sure that you have SSH Key installed and have direct root access.
Mention the webservers and dbservers in hosts file and run the playbook using
the below command:

        ansible-playbook -v -i hosts site.yml

Once done, you can check the results by browsing to http://ipaddress/.
You should see a simple test page and a list of databases retrieved from the
database server.

to test php installation navigate to http://ipaddress/phpinfo.php
