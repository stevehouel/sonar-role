# Sonar Creation playbook #


## Requirements

This project must be cloned under specific project's Ansible Roles to Create Sonar Container.

## Variables

`sonar_path` : Sonar Root Path for configurations and datas

`sonar_data_path` : Sonar Data Path (usually set to "{{ sonar_path }}/data")

`sonar_plugins_path` : Sonar Plugins Path (usually set to "{{ sonar_path }}/plugins")

`sonar_port` : Listen port on Docker host to map to Sonar container

`sonar_jdbc_database` : Database Name for Sonar datas

`sonar_jdbc_url` : Jdbc URL for Sonar. Usually set to "jdbc:postgresql://{{ sonar_postgresql_url }}:{{ sonar_postgresql_port }}/{{ sonar_jdbc_database }}?useUnicode=true&characterEncoding=utf8"

`sonar_version` : Sonar image version

`sonar_jdbc_username` : Database Username for Sonar

`sonar_jdbc_password` : Database Password for Sonar

`sonar_postgresql_url` : Database URL (postgresql)

`sonar_postgresql_root_username` : Postgresql Root username (used to create Sonar specific user)

`sonar_postgresql_root_password` : Postgresql Root Password

`sonar_postgresql_port` : Postgresql Database Port


## Files

* You need to create a folder with path `conf-sonar/plugins` to include all plugins (jar files) for the sonar servers.
