# Databases

* Relational
* No sQL
* Cache

*Dynamo db

* Cacheing => Redis cache=> Radis cache,Elastic Cache

# Hard Disks Or SSD

* ebs
* speed
# Mounting EBS volume
```
sudo lsblk
sudo mkfs -t ext4 /dev/xvdf
sudo mount /dev/xvdf /home/ec2-user
```

* To create file system/Format
```
sudo mkfs -t ext4 /dev/xvdf
```

* Mounting
```
sudo mount /dev/xvdf /home/ec2-user
```
[AWSDOCS](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html)

fstab perminent mounting

* disk is change while running instance alo  [clickhere](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/recognize-expanded-volume-linux.html)

* more speed =More iops
# EFS 

sudo mount -t efs fs-e5692b9c:/ /efs
* Network storage
# HardDisk
* Taking a backup of hard disk snapshot

hardisks region\
snapshot availabulity zone

create snapshot
from snapshot create vole
create snapshot to another regon


How to mount ebs to docker volume?
