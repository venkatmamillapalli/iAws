# Queries

COmmand to configure aws

```
aws configure
```
Command to query security group ids

```
aws ec2 describe-security-groups --query "SecurityGroups[].GroupId"
```