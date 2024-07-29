# CLOUD COMPUTING DRAWINGS

---

## Simple VPC Architecture

### Description

This is an architecture that involves the creation of an AWS VPC which plans two availability zones in a region. Resources such as four EC2 instances, four subnets, two security groups, two route tables, internet gateway and NAT gateway.

The VPC spans two availability zones. There are two public subnets, one for each availability zone. The same thing applies to the two private subnets. An internet gateway provides internet access to the VPC. A public route table routes all internet related traffic to the internet gateway. This route table is associated with the two public subnets. A NAT gateway, which is associated with the public subnet 1 forms the destination of the internet bound routes from the private subnets. This routing is held by the private route table. Security levels are added by using NACLs for the public and private subnets as well as security groups for the individual EC2 instances in the subnets.