# Ansible-EC2-Instance
Ansible Role to manage EC2 instances.
# Requirements
The below requirements are needed on the host that executes this module.
 - boto
 - boto3
 - python >= 2.6
 - Ansible >= 2.4
 
# Role Variables
Just a couple of examples can be seen below, see [defaults/main.yml](defaults/main.yml) for the full list.

```
- name: Provision an EC2 Instance
  hosts: localhost
  connection: local
  gather_facts: False
  tags: provisioning
  # Necessary Variables for creating/provisioning the EC2 Instance
  vars:
    instance_type: t2.micro
    security_group: ansible
    image: ami-82be18ed
    keypair: id_rsa
    region: eu-central-1
    count: 1
    ec2tag: yourtag
    sec_grp_in:
      - proto: tcp
        from_port: 22
        to_port: 22
        cidr_ip: 0.0.0.0/0
      - proto: tcp
        from_port: 443
        to_port: 443
        cidr_ip: 0.0.0.0/0
```
# Author Information

You can find me on Twitter: [@itkombinat](https://twitter.com/itkombinat)
