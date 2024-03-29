- Establish connectivity between VPCs and AWS services without exposing data to the internet
- provides **private connectivity** between virtual private clouds (VPCs), supported AWS services, and your on-premises networks without **exposing your traffic to the public internet**.
- Using VPC endpoints can be handy in situations like the following:
	- If you want to connect your VPC to another AWS VPC but do not have VPN or TGW access
	- The other VPC has an overlapping IP address with your VPC
	- You want to share your VPC with external customers but do not want traffic to leave the AWS network
![[PrivateLink.png]]
- VPC endpoint service
	- you need network load balancer or Gateway load balancer
	- Services created on NLB can be accessed using interface endpoints
	- Services created on GLB can be accessed using Gateway load balancer end points
- Interface VPC endpoints
	- VPC endpoints provide secure access to a specific service,
	- VPC endpoints provide access to a specific service without the need of using any other gateways – no need to use an Internet gateway, a NAT gateway, a VPN connection, or a VPC peering connection, reducing the risks of exposing your resources to the Internet or to other outside network
-  VPC endpoint services
	- Interface endpoints
	- Gateway endpoints
- **VPC Security Groups can be used** to manage access to the endpoints.
- Sharing your services over AWS PrivateLink
- **Privately connecting to your on-premises applications**
- Integration with AWS Marketplace
- Gateway endpoints
	- Currently, AWS S3 and DynamoDB are the only services supported by gateway endpoints
- **VPC interface endpoints vs gateway endpoints**
	- Charge
		- billed
		- not billed
	 - Access from on-premises
		 - allow access from on-premises
		 - no access from on-premises
	 - Support
		 - most of the AWS services
		 - Supports only S3 and DynamoDB
	 - Association
		 - associated on Subnet level
		 - on a VPC
        - Other
	        -  
	        - must be inside VPC
	- cross region
		- **allow cross region through VPC peering or TGW**
		- not allowed