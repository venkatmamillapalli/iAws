# Networking

## What is VPC?
A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC

When you create a VPC, you must specify a range of IPv4 addresses for the VPC in the form of a Classless Inter-Domain Routing (CIDR) block; for example, 10.0.0.0/16. This is the primary CIDR block for your VPC

## What is Subnet?
A VPC spans all the Availability Zones in the region. After creating a VPC, you can add one or more subnets in each Availability Zone. When you create a subnet, you specify the CIDR block for the subnet, which is a subset of the VPC CIDR block. Each subnet must reside entirely within one Availability Zone and cannot span zones. Availability Zones are distinct locations that are engineered to be isolated from failures in other Availability Zones. By launching instances in separate Availability Zones, you can protect your applications from the failure of a single location. We assign a unique ID to each subnet.

## RouteTable
A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet is directed.

The following are the key concepts for route tables.

Main route table—
The route table that automatically comes with your VPC. It controls the routing for all subnets that are not explicitly associated with any other route table.

Custom route table—A route table that you create for your VPC.

Route table association—The association between a route table and subnet. The route table that's associated with a subnet controls the routing for that subnet.

Destination—The destination CIDR where you want traffic from your subnet to go. For example, an external corporate network with a 172.16.0.0/12 CIDR.

Target—The target through which to send the destination traffic; for example, an internet gateway.

Local route—A default route for communication within the VPC.

## Internet Gateway

An internet gateway is a  VPC component that allows communication between instances in your VPC and the internet.

An internet gateway supports IPv4 and IPv6 traffic.

[Formore](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)

## Egress Only Internet Gateway

An egress-only Internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows outbound communication over IPv6 from instances in your VPC to the Internet, and prevents the Internet from initiating an IPv6 connection with your instances.

#### Note
An egress-only Internet gateway is for use with IPv6 traffic only. To enable outbound-only Internet communication over IPv4, use a NAT gateway instead.

## Elastic IP Addresses
An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is associated with your AWS account. With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account.

An Elastic IP address is a public IPv4 address, which is reachable from the internet. If your instance does not have a public IPv4 address, you can associate an Elastic IP address with your instance to enable communication with the internet; for example, to connect to your instance from your local computer.

## NAT GateWay
You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances

[AWS Docs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)

## VPC Peering

A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection).

[AWS Docs](https://docs.aws.amazon.com/vpc/latest/peering/create-vpc-peering-connection.html)