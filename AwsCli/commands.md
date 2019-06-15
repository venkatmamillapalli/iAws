* To create VPC net work

```
aws ec2 create-vpc --cidr-block 192.168.0.0/16

```
* To Create Subnet
```
aws ec2 create-subnet --vpc-id vpc-0722682c17c9145ed --cidr-block 192.168.0.0/24 --availability-zone us-east-2a

```