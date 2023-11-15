# [VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) - Virtual Private Cloud

- Subnets: Tied to an AZ, Network Partition of the VPC
- Internet Gateway: Provide internet access at VPC level
- [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html): A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.
- NACL: Network Access Control List - Stateless, subnet rules for inbound and outbound
- Security Groups: Stateful, operate at the EC2 level
- VPC Peering: Connect two VPC with Non overlapping IP Ranges, non transitive
- VPC Endpoints: Provide private access to AWS Services within VPC
- VPC Flow Logs: Network Traffic Logs
- Site to Site VPN: VPN Over public internet between on-premises DC and AWS
- Direct Connect: Direct Private Connection to AWS 