# aws-notes


# AMI:

Amazon Machine Image is region specific resource <br>
Multiple EC2 instances can be deployed using the same AMI <br>
AMI created in one region will not be available in another region, however it is possible to share/copy the AMI to other regions. <br>
AMI can be copied to other regions in the same AWS account <br>
AMI can be shared to other regions in the same or other AWS accounts also. <br>

# Key Pair:
EC2 Key-Pair is region specific resource <br>
One Key-Pair can be associated with multiple EC2 instances, where as one EC2 instance cannot have more than one Key-Pair associated. <br>
Key-Pair created in one region will not be available on other regions. <br>
Key-Pairs cannot be copied/shared to other regions <br>

# Elastic IPs:
Elastic IP is region specific resource <br>
One EIP can be associated with one network interface only, however it’s possible to de-associate and associate to another network interface within the same region. <br>
EIP cannot be copies/shared to other regions <br>

# EBS Volume:
EBS volumes are Availability Zone specific resources <br>
EBS volume cannot be span multiple AZs <br>
EBS volume must be created in same AZ where EC2 created to attach the volume to the instance. <br>
EBS volume can be attach to multiple EC2 instances, but only selected types of EBS volumes are supported for this feature to work with clustered apps. <br>

# Security Group:
Security Groups are VPC specific resources <br>
One Security Group can be associated with multiple EC2 instances with in the same VPC. <br>
Security Group cannot be associated with resources in different VPC. <br>
Security Groups are stateful and works at EC2/RDS/ELB level. <br>

# Network ACL:
NACL is VPC specific resource <br>
NACL is Stateless and can only be associated with subnets. <br>
One NACL can be associated with multiple subnets, however one Subnet can have only one NACL. <br>

# Internet Gateway:
Internet Gateways are region specific resource <br>
Internet Gateways must be associated with only one VPC. <br>
VPC must be associated with only one IGW <br>
IGW cannot span multiple VPC <br>

# Route Table:
Route Tables are VPC specific resources <br>
Route Tables must be associated with subnets only. <br>
One Route Table can associate with multiple subnets; however, one Subnet can have only one Route Table. <br>
Route Tables cannot span VPCs <br>

# VPC:
VPC is region specific resource <br>
Instances deployed into one VPC can communicate each other via local GW by default. <br>
Communication between the VPCs not possible by default. <br>
VPC Peering or Transit Gateway is required to provide communication between the VPCs. <br>
VPC cannot span multiple regions <br>

# Subnets:
Subnets must be associated with one Availability Zone. <br>
One Subnet can associate with one AZ only, however one AZ can have multiple subnets. <br>
Subnets cannot span multiple AZs. <br>
