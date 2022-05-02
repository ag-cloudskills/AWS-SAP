# EC2 Networking

- Primary ENI ( lifetime)
- Secondary ENI  ( different subnet possible. not diff AZ), it can be de-attached and attached
- SG is attached with ENI , not EC2
- each interface is allocated IPV4 and it will remain same throughout the life
- Public Ip is not visible to OS
- Elastic IP are static public IP
- IPV6 public address are configured on OS
- source destination check configuration can be enabled and disabled as per requirment
- Isolated networks can be created using different ENI
- MAC address based licensing can be used via ENI