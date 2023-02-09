# Website

Description: Provisioning and configuring infrastructure through automation

### Tasks:

- Launch an EC2 instance

- Configure the web server to serve a static website

Using the MacOS terminal with pre-installed AWS CLI, and pre-configured IAM role, vpc (virtual private cloud), subnet, security group, route table, and Network ACL. The following script launches an ec2 instance into a virtual machine.

```bash
aws ec2 run-instances --image-id ami-0aa7d40eeae50c9a9 (64-bit (x86)) --count 1 --instance-type t2.micro \
--key-name my-keyname --subnet-id subnet-00xxxxxxxx --security-group-ids sg-00xxxxxxxx \
--user-data echo "This is a static web server"
```

