# ec2-ansible-redis

This playbook addresses the topic of starting redis cluster in AWS.

Prereq would be
- ansible installed locally 
- boto python module.
- aws credentials set (~/.aws/credentials)
E.g. credentials:
[default]
aws_access_key_id = (your key id)
aws_secret_access_key = (your access key)

To run it for your case, please check the group_vars/all.yml file and fill the variables accordingly.
Exaplanations:
stack_region - where your instances will be created 
type_of_instance - type for your instances
key_pem_name - name of the key that will used/created
aws_image - image/ami for your instances
aws_user - user that will be used to connect to the aws instances
security_group - the security group name that will be used/created
number_of_servers - number of redis slaves + redis master
port_redis - port used for redis communication

Top run the playbook run the command: ansible redis.yml
