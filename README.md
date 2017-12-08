[![Build Status](https://travis-ci.org/alesium/ansible-smartos-ipfilter.svg)](https://travis-ci.org/alesium/ansible-smartos-ipfilter)

smartos-ipfilter
=========

Ansible Role to configure ipfilter for smartos

Requirements
------------

- Hosts should be bootstrapped for ansible usage (have python,...)
- Root privileges, eg `become: yes`

Role Variables
--------------

| Variable | Description | Default value |
|----------|-------------|---------------|
| `smartos_ipfilter_service_name` | Service name for handlers | `"network/ipfilter"` | 
| `smartos_ipfilter_ipf_config_file_src` | ipf.conf local template location | `"ipf.conf.j2"` | 
| `smartos_ipfilter_ipf_config_file_dest` | ipf.conf remote location | `"/etc/ipf/ipf.conf"` | 
| `smartos_ipfilter_ipnat_config_file_src` | ipnat.conf local template location | `"ipnat.conf.j2"` | 
| `smartos_ipfilter_ipnat_config_file_dest` | ipnat.conf remote location | `"/etc/ipf/ipnat.conf"` | 

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: sperreault.smartos-ipfilter }

License
-------

BSD

Author Information
------------------

Sebastien Perreault <sperreault@alesium.net>
