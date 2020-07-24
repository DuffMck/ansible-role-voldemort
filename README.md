Ansible Voldemort Role
=========

Install and config [Voldemort server](https://www.project-voldemort.com/voldemort/)

Requirements
------------

Python installed on target machine

Role Variables
--------------

Required variables:
```yml
installation_name: your installation name
```

Optional variables with defaults:
``` yml
# vars used in CONFIG_FOLDER/cluster.xml
voldemort_cluster_ip: 0.0.0.0
voldemort_cluster_http_port: 8081
voldemort_cluster_socket_port: 6669
voldemort_cluster_admin_port: 6668

# vars used in CONFIG_FOLDER/server.properties
voldemort_mysql_host: localhost
voldemort_mysql_port: 1521
voldemort_mysql_user: root
voldemort_mysql_password: 3306
voldemort_mysql_database: test
```


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: duffmck.ansible-role-voldemort, installation_name: test }

License
-------

MIT
