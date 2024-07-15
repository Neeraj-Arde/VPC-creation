# VPC-creation

```bash
Virtual Private Cloud:
VPC is your on Private cloud in which you will deploy all of your resources including Instances, RDS and multiple similar services.
We can deploy multiple VPC in a single account. Basically you can bifurcate you enviroment such as UAT, pre-pord, Prod as your requirement.
For creating we will require a CIDR range.
VPC is consists of Subnets, Route Tables, Gateways and VPN.
```

```bash
Subnet:
There are 2 types on subnets Private and Public.
Subnet which is having an internet gateway is called Public Subnet. It is able to access internet.
Private subnet dosent have internet gateway so it can not have directly access to the internet, it will require a NAT gatewayto commumnicate with other resources and interbet as well but it depends upon NAT configuration. NAT connectivity should be public to access the internet.
Route table of Public subnet should consist igw in it and Private subnet will be having NAT.
```

```bash
#Security
There are 2 levels of security we can provide in VPC which are Network access control list (NACL) and Security Group (Sg)
NACL work on VPC level: Consists of Inboud/outbount Rules Block incoming traffic directly from entering VPC.
Sg works on resource level: Consists of Inboud/outbount Rules Block incoming traffic at resource level.

```

#Create VPC Step by step

```bash
Serach for VPC and select
Click on create VPC
Select VPC and more
Name Tag Auto Generate: It will name all the internal resources according to the Name which you will provide here
Select required IPv4 CIDR block (eg. 10.0.0.0/16)
Select tenency accordingly: Defualt will share your resources on host on AWS side and dedicated will allow you to use a whole resource but it will charge you for complete host.
Select numbers on AZ you require
Select number of Public and Private subnet.
Select NAT gateway configuration.
VPC endpoint can be created later as requirement.
```
