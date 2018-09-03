Ansible-EC2-Instance
=========


Role Variables
--------------

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
```
Author Information
------------------

IT-KOMBINAT.ORG
