Ansible Cobalt Strike (Docker)
=========

[![t94j0.mythic](https://img.shields.io/ansible/role/55834)](https://galaxy.ansible.com/warhorse/cobaltstrike-docker)


Install Cobalt Strike (Docker)

Role Variables
--------------

A list of all the variables can be found in ./defaults/main.yml.

`cs_dir` - Cobalt Strike container directory 
`cs_ports` - Cobalt Strike container ports to open
`cs_hostname` - Cobalt Strike container hostname
`cs_container_name` - Cobalt Strike container name 
`cs_key` - Cobalt Strike teamserver License Key (REQUIRED)
`cs_password` - Cobalt Strike teamserver password (REQUIRED)
`cs_exp_date` - Cobalt Strike becon expiration date (REQUIRED)
`cs_profile` - Location of your Cobalt Strike 
`cs_docker_network` Cobalt Strike container docker network


Dependencies
------------

ansible-galaxy install geerlingguy.docker
ansible-galaxy install geerlingguy.pip

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - { role: warhorse.cobaltstrike-docker }
```

Example Vars
----------------

```yaml
cs_hostname: "cobaltstrike"
cs_container_name: "cobaltstrike"
cs_key: '000-000-000-000-000'
cs_password: 'Password'
cs_exp_date: '2020-12-20'
cs_profile: 'clean.profile.j2'
cs_docker_network: "cobaltstrike"
cs_dir: '/opt/docker/cobaltstrike'
cs_ports:
  - "50050:50050"
  - "80:80"
  - "443:443"
```

License
-------

BSD

Author Information
------------------

Ralph May <>
