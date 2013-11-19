Easy CloudFormation
===================

CloudFormation is an amazon tool to help orgnizaiton to reduce the effort of the Ops.
Althrough there are millions of application, most of them share similar archtecture, such as
ELB, auto scaling.

If you are doing something similar, this tool will help you.

Example
==================
* create a app.yml to contain following information:
```
app_name: Easy CloudFormation
zone_name: testing.easycloudformation.com
vpcid: vpc-12345678
public_subnets:
  - subnet-01234567
  - subnet-12345678
private_subnets:
  - subnet-23456789
  - subnet-34567890
auto_scaling:
  scale_up: 80
  scale_down: 35
image_id: ami-316cfc0b
install_script: install.sh
```

* provision whole env
```
rake provision
```
