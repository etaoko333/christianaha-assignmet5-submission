find below my christinah alonge submission for assignment5
## Key learnings, experience and your main selling points.

This section will be used to write your profile for your CV. So record your key learnings and experience on a weekly basis so we can track your progress and learning.

| Number      |           Subject              | What you have learnt this week and how might you describe this at an interview?   |
| :---        |            :----:              | :---  |
| 1  | Collaboration                           | YYYYYYYY   |
| 2  | Communication                           | YYYYYYYY   |
| 3  | Automation/CICD                         | YYYYYYYY   |
| 4  | AWS                                     | YYYYYYYY   |
| 5  | Kubernetes                              | YYYYYYYY   |
| 6  | Terraform                               | YYYYYYYY   |
| 7  | Linux                                   | YYYYYYYY   |
| 8  | System and Application Design           | YYYYYYYY   |
| 9  | Productivity                            | YYYYYYYY   |
| 10 | Yourself and your abilities             | YYYYYYYY   |


## Kubernetes, Docker, Containerisation and Virtualisation

1. What are Kubernetes Operators? 	What are Kubernetes Operators? A Kubernetes operator is an application-specific controller that extends the functionality of the Kubernetes API to create, configure, and manage instances of complex applications on behalf of a Kubernetes user.
2.	What are Kubernetes CRD? A custom resource definition (CRD) is a powerful feature introduced in Kubernetes 1.7. The standard Kubernetes distribution ships with many built-in API objects and resources. CRDs enable IT admins to introduce unique objects or types into the Kubernetes cluster to meet their custom requirements.
3.	What are Kubernetes Controllers Kubernetes, controllers are control loops that watch the state of your cluster, then make or request changes where needed. Each controller tries to move the current cluster state closer to the desired state.


2. 
## Linux administration and shell scripting

Research the following Linux commands

1. 1.	tar 	is used for saving several files into an archive file.
2.	rsync	is a command-line tool for copying files and directories between local and remote systems.
3.	chown	The chown command changes the owner of the file or directory specified by the File or Directory parameter to the user specified by the Owner parameter.
4.	curl	. It communicates with a web or application server by specifying a relevant URL and the data that need to be sent or received.
5.	systemctl	command manages both system and service configurations, enabling administrators to manage the OS and control the status of services.
6.	Useradd command creates a new user account.
7.	Usermod It is used to modify existing user account details, such as username, password, home directory location, default shell, and more.
8.	ln	command is used to create links to files or directories.
9.	chmod	command is used to change permissions for a file or directory on a Unix machine.
10.	chage	command changes the number of days between password changes and the date of the last password change. This information is used by the system to determine when a user must change their password


11. Explain what the following command does.
```
ssh-keygen -f mykeyfilename -t rsa -b 4096 ans: ssh-keygen: This is the command-line tool used for generating SSH keys.

-f mykeyfilename: The -f option specifies the filename for the generated SSH key pair. In this case, it is set to "mykeyfilename". The generated key pair will consist of two files: "mykeyfilename" (private key) and "mykeyfilename.pub" (public key).

-t rsa: The -t option specifies the type of key to generate. In this case, it is set to "rsa", indicating that an RSA key pair will be generated. 

-b 4096: The -b option specifies the number of bits in the key. In this case, it is set to "4096", indicating that the RSA key pair will have a key size of 4096 bits. Larger key sizes provide increased security but may also result in slightly slower performance during encryption and decryption operations.

```
12. Explain what these permissions bits mean and translate them into the corresponding numeric value.
r: Read permission
w: Write permission
x: Execute permission
-: No permission

```
1 -rwxrwxrwx The first character - indicates that it is a regular file.
The next three characters rwx represent the owner's permissions, which are read, write, and execute.
The following three characters rwx represent the group's permissions, which are also read, write, and execute.
The last three characters rwx represent permissions for others, which are read, write, and execute. Translated into numeric value: 777
2 -rw-r-xr-x 

-rw-r-xr-x The first character - indicates that it is a regular file.
The next two characters rw represent the owner's permissions, which are read and write.
The following three characters r-x represent the group's permissions, which are read and execute.
The last three characters r-x represent permissions for others, which are read and execute.
Translated into numeric value: 754
3 -r--r--r---r--r--r-- The first character - indicates that it is a regular file.
The next character r represents the owner's permission, which is read only.
The following two characters -- represent the group's permissions, which have no permission.
The last three characters r-- represent permissions for others, which are read only.
Translated into numeric value: 444



13. Which of these bits relate to symbolic link and which to a directory and which a simple file?
```
1 drwxrwxrwx drwxrwxrwx corresponds to a directory.
2 lrw-r-xr-x corresponds to a symbolic link.
3 -r--r--r-- corresponds to a regular file.
```


## CICD, Infrastructure as as Code (IaC), Terraform, Packer and Ansible


1. A simple three-tier java based application is deployed across two availability zones(AZ) on a Tomcat server. The application uses a self-managed PostgresQL database as its persistence layer and Nginx as its web server. The application is not required to be highly resilient nor be capable of elastic behaviour.

*  Describe how you might build this environment manually from the tool chain you are familiar with. ans: 1.	Describe how you might build this environment from an automated provisioning pipeline from the tool chain you are familiar with. Ans: Provisioning the Infrastructure:
•	Select two availability zones (AZ) in your chosen cloud provider.
•	Manually create Virtual Private Cloud (VPC) in each AZ.
•	Configure subnets within each VPC, ensuring they are spread across different availability zones.
•	Create security groups to define inbound and outbound traffic rules for the instances.
•	Launch instances in the desired AZs using an Amazon Machine Image (AMI) that includes the operating system and pre-installed Tomcat and Nginx.
•	Assign appropriate security groups, subnets, and availability zones to each instance.
•	Configure the instances to automatically start Tomcat and Nginx upon boot.
2.	Setting up the Database:
•	Launch a separate instance in one of the availability zones to host the PostgreSQL database.
•	Configure security groups and subnets for the database instance.
•	Install and configure PostgreSQL on the instance.
•	Create the necessary database and user accounts for your application.
3.	Configuring Nginx:
•	Access the instance running Nginx via SSH.
•	Install Nginx on the instance.
•	Configure Nginx as a reverse proxy to forward requests to the Tomcat instances.
•	Set up any required SSL/TLS certificates for secure communication.
4.	Deploying the Java Application:
•	Build your Java application code, creating a deployable artifact such as a WAR file.
•	Copy the artifact to each Tomcat instance using SCP or a similar file transfer method.
•	Configure the Tomcat instances to deploy the application and start it.
5.	Testing and Verification:
•	Test the connectivity between the Nginx server, Tomcat instances, and the database.
•	Ensure the application is accessible through the Nginx server's public IP or domain name.
•	Validate that the application can interact with the PostgreSQL database.
6.	Monitoring and Logging:
•	Set up monitoring and logging tools to track the performance and health of your infrastructure and application.
•	Configure alerts and notifications for critical events or anomalies.
Remember to secure your infrastructure, enable backups, and follow best practices for network and instance-level security.
While this manual process provides a general overview, it's worth noting that automating the infrastructure provisioning process through Infrastructure as Code (IaC) tools like Terraform or AWS CloudFormation can greatly streamline and enhance the reproducibility of the environment setup.

*  Describe how you might build this environment from an automated provisioning pipeline from the tool chain you are familiar with.

2. Considering question 1 above, how would you re-design the application so that it is both elastic and highly available across the three tiers?

3. Describe how you would use Maven to build a java application ans:
2.	Install Maven: Download and install Maven on your machine if you haven't already. You can find the installation instructions for your operating system on the Apache Maven website (https://maven.apache.org/install.html).
3.	Generate a Maven Project: Open a terminal or command prompt and navigate to the directory where you want to create your project. Use the following command to generate a Maven project structure:
arduinoCopy code
mvn archetype:generate -DgroupId=com.example -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false 
This command generates a basic Maven project structure with a standard directory layout.
1.	-DgroupId: Specifies the group ID for your project. It is typically based on your organization's domain name but can be any unique identifier.
2.	-DartifactId: Specifies the artifact ID for your project. This is the name of your application.
3.	-DarchetypeArtifactId: Specifies the Maven archetype to use for project generation. In this case, we are using maven-archetype-quickstart which sets up a basic Java project.
4.	Navigate to the Project Directory: Once the project generation is complete, navigate to the project directory using the following command:
bashCopy code
cd my-app 
5.	Build the Project: Now, you can build your Java application using Maven. Maven uses a default lifecycle with various phases like compile, test, package, etc. Use the following command to build your project:
Copy code
mvn clean install 
This command will compile your source code, run tests, and package your application into a JAR file.
1.	clean: This is an optional phase that cleans the target directory before building.
2.	install: This phase compiles, tests, and packages the application and then installs it into the local Maven repository for use by other projects.
After successful execution, you will find the compiled JAR file in the target directory.
6.	Additional Maven Commands: Maven provides several other commands and options to customize the build process. Some commonly used commands include:
1.	mvn clean: Cleans the target directory, removing all generated files.
2.	mvn test: Runs the tests for the project.
3.	mvn package: Packages the application into a JAR or other desired format.
4.	mvn dependency:tree: Displays the project's dependency tree.

## System Architecture and Application Design, Cloud Computing (AWS)

| Number      |           Subject                | Role       |

| :---        |            :----:                | :---       |
| 1  | Global backbone                           | The global backbone refers to the network infrastructure and high-speed connections that interconnect AWS regions and availability zones. It ensures reliable and low-latency connectivity between different regions and availability zones.   |
| 2  | Region                                    | Region	A region is a geographic area where AWS resources are located. Each region consists of multiple availability zones and is designed to be isolated from other regions, allowing customers to deploy resources in specific geographical locations for redundancy and low latency.   |
| 3  | Availability zone (AZ)                    | Availability zone (AZ)	An availability zone (AZ) is a data center facility within a region that is isolated and physically separate from other availability zones. Each availability zone has redundant power, networking, and cooling infrastructure to ensure high availability and fault tolerance for AWS services.
4	   |
| 4  | Point of Presense (PoP)                   | Point of Presence (PoP)	A point of presence (PoP) refers to an edge location or data center facility where AWS places its content delivery servers (CDN) and caching servers. These PoPs help deliver content and improve latency by caching and serving static and dynamic content closer to end users.   |
| 5  | Co-location                               | Co-location refers to the practice of housing privately-owned servers and network equipment in a third-party data center facility. AWS offers co-location services that allow customers to place their own hardware in AWS data centers, leveraging AWS's infrastructure and connectivity.   |
| 6  | Direct Connect                            | AWS Direct Connect is a service that provides dedicated and private network connectivity between an on-premises data center and AWS. It allows customers to establish a high-bandwidth and low-latency connection, bypassing the public internet, for improved security, performance, and cost savings.   |
| 7  | VPC                                       | A Virtual Private Cloud (VPC) is a logically isolated virtual network within AWS. It allows customers to define and control their own virtual network environment, including IP address ranges, subnets, route tables, and network gateways. VPC provides a secure and private environment for running AWS resources.   |
| 8  | Subnet                                    | A subnet is a range of IP addresses within a VPC. It is a subdivision of a VPC and allows for further segmentation of the network. Subnets can be public or private, and resources within a subnet can communicate with each other using private IP addresses.   |
| 9  | AWS Public domain service                 | AWS Public domain service:	AWS public domain services refer to the various cloud services provided by AWS, such as EC2, S3, RDS, DynamoDB, etc. These services are accessible to the public and can be used by customers to build and deploy their applications in the AWS cloud environment.   |
| 10 | Internet gateway                          | Internet gateway:	An internet gateway is a horizontally scalable AWS-managed service that allows communication between a VPC and the internet. It serves as a gateway to connect VPC resources to the internet, enabling outbound and inbound internet traffic to and from the VPC.   |
| 11 | NAT                                       | Network Address Translation (NAT) is a service that allows private subnets within a VPC to initiate outbound internet traffic while keeping the instances within the private subnets hidden behind the NAT gateway or NAT instance. It provides a secure way for private instances to access the internet.   |
| 12 | Bastion server                            | A bastion server, also known as a jump box or jump host, is a securely configured server that acts as a gateway to access and manage instances in private subnets. It provides a controlled and monitored entry point for administrators to establish secure remote connections to the private instances. |

2.  What role does the following AWS components play in a typical Three-tier Application design. ans: 

| Number      |           Component              | Role       |
| :---        |            :----:                | :---       |
| 1  | External Load balancer                           | stands for network address translation. It's a way to map multiple private addresses inside a local network to a public IP address before transferring the information onto the internet.   |
| 2  | Internal Load balancer                           | Internal Load balancer:	Internal load balancers are used to load balance traffic inside a virtual network.   |
| 3  | Multiple Availability zones (AZ)                 | (AZ)	Availability zones are multiple, isolated locations within a region, and a region is a geographical location with multiple availability zones mapped within it. Every region is isolated and independent from every other region.   |
| 4  | Auto-scaling group                               | An Auto Scaling group contains a collection of EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management.   |
| 5  | Web tier                                         | is an optional component that allows users to connect to the Service Manager server through a Web browser.   |
| 6  | Application tier                                 | Application tier:	is the heart of the application. In this tier, information collected in the presentation tier is processed - sometimes against other information in the data tier - using business logic, a specific set of business rules.   |
| 7  | Database (Master)                                | Database: (Master)	 is a modern, powerful, intuitive and easy to use database query, administration, and management software with a consistent.   |
| 8  | Database (Slave)                                 | enables data from one database server (the master) to be replicated to one or more other database servers (the slaves).   |


3. An AWS customer wants to connect their on-premise datacenter to their VPC network in AWS. Describe the ways in which this could be achieve? ans:	AWS Direct Connect:
•	AWS Direct Connect establishes a dedicated network connection between the on-premises datacenter and AWS. This provides a private, dedicated connection with higher throughput and lower latency compared to internet-based connections.
•	The customer needs to set up a Direct Connect location, which can be done by working with an AWS Direct Connect Partner or using AWS Direct Connect Gateway for a multi-account or multi-VPC setup.
•	A Direct Connect gateway can be used to enable connectivity to multiple VPCs within the AWS account.
•	Direct Connect supports various bandwidth options and can be provisioned with redundant connections for high availability.
2.	VPN Connection:
•	AWS VPN (Virtual Private Network) allows for an encrypted connection over the internet between the on-premises datacenter and the AWS VPC.
•	This method is suitable for scenarios where lower bandwidth requirements are acceptable, and the data transfer is not highly sensitive to latency.
•	AWS offers two types of VPN connections: Site-to-Site VPN and AWS Client VPN.
•	Site-to-Site VPN: This establishes a secure connection between the on-premises VPN device (customer gateway) and the AWS VPN endpoint (virtual private gateway). It can use either IPsec or AWS Transit Gateway for connectivity.
•	AWS Client VPN: This provides secure remote access to the AWS resources from on-premises networks using OpenVPN-based clients.
3.	AWS Transit Gateway:
•	AWS Transit Gateway is a highly scalable and managed service that simplifies network connectivity across multiple VPCs, on-premises networks, and AWS accounts.
•	By connecting the on-premises datacenter to a Transit Gateway, the datacenter can communicate with any VPC attached to the Transit Gateway, providing a hub-and-spoke architecture.
•	The on-premises network is connected to the Transit Gateway using VPN or Direct Connect connections.
•	Transit Gateway provides simplified routing, central control, and management of network traffic.
3.	
An AWS customer can build services using components from the AWS public domain as well as services deployed in the customer's VPC and datacentre. 

4. Name some AWS services that run in the public domain and how they might be integrated with services in the VPC and in the on-premises datacentre. ans: 
AWS provides a wide range of services that run in the public domain and can be integrated with services deployed in a customer's VPC and on-premises datacenter. Here are some AWS services and how they can be integrated:
1.	Amazon S3 (Simple Storage Service):
•	Amazon S3 is a highly scalable object storage service that allows customers to store and retrieve data from anywhere on the web.
•	Integration: Services running in the VPC or on-premises datacenter can interact with S3 by leveraging the AWS SDKs or APIs. They can upload/download files, store backups, or share data between different environments.
2.	Amazon RDS (Relational Database Service):
•	Amazon RDS provides managed database services for various relational databases such as MySQL, PostgreSQL, Oracle, and SQL Server.
•	Integration: Applications running in the VPC or on-premises datacenter can connect to an Amazon RDS database instance over the internet using the appropriate database client drivers. This allows for seamless data access and management.
3.	Amazon EC2 (Elastic Compute Cloud):
•	Amazon EC2 offers resizable compute capacity in the cloud, allowing customers to launch virtual servers known as instances.
•	Integration: Instances running in the VPC or on-premises datacenter can communicate with EC2 instances using private IP addresses or public IP addresses. This enables application components to interact with each other across environments.
4.	AWS Lambda:
•	AWS Lambda is a serverless computing service that allows running code without provisioning or managing servers.
•	Integration: Lambda functions can be triggered by various events within the VPC or on-premises datacenter, such as changes in S3 buckets, updates in databases, or API calls. Lambda functions can process the events and perform specific tasks or initiate actions across different environments.
5.	Amazon API Gateway:
•	Amazon API Gateway enables the creation, deployment, and management of APIs.
•	Integration: API Gateway can serve as a frontend for services running in the VPC or on-premises datacenter, allowing secure and controlled access to these services via APIs. It acts as a bridge between different environments, providing a unified interface for external clients.
6.	AWS Direct Connect:
•	AWS Direct Connect provides a dedicated network connection from the customer's datacenter to AWS.
•	Integration: Direct Connect allows for a private and dedicated connection between on-premises datacenters and the VPC. This facilitates secure and low-latency communication between services running in the customer's environment and AWS resources.

5. With respect to AWS cloud services explain what each of these mean;
•	Infrastructure as a Service (IAAS) IaaS is an effective cloud service model for workloads that are temporary, experimental or that change unexpectedly.
•	Platform as a service (PAAS) Platform as a service (PaaS) is a cloud computing model where a third-party provider delivers hardware and software tools to users over the internet.
•	Software as a service (SAAS) software-as-a-Service (SaaS), is a cloud-based software delivery model that allows end users to access software applications over the internet.
•	Managed services	 tasks handled by a third party, frequently in the context of business information technology services. The managed services model is a way to offload general tasks to an expert in order to reduce costs, improve service quality, or free internal teams to do work that's specific to their business.
•	Serverless services	Serverless is a cloud-native development model that allows developers to build and run applications without having to manage servers.
•	Self-managed services: services are tasks handled by a third party, frequently in the context of business information technology services.

6. In terms of their geographical location and distribution, AWS services can be roughly categorised as Global, Regional and Zonal. What do you understand by this classification?  
7. Complete the table below, naming some services in the corresponding category
Number	Global services	Regional services	Zonal services

| Number	Global services	   Regional services	      Zonal services
1	     Amazon S3	        Amazon RDS	               Amazon EC2
2	     Amazon DynamoDB	  Amazon Redshift	           Amazon EBS
3	     AWS IAM	          Amazon CloudFront	         Amazon Elastic Load Balancer
4	     AWS Lambda	        AWS Step                    Functions	AWS Fargate
5	     Amazon Route 53	  AWS Glue	                  Amazon EC2 Auto Scaling
6	     Amazon SQS	        AWS CodePipeline	          AWS Batch
7	     AWS CloudFormation	Amazon Aurora	              Amazon ElastiCache
8	     Amazon SNS	        AWS AppSync	                AWS Elastic Beanstalk
9	     AWS CloudTrail	    Amazon Elastic Transcoder	  AWS Storage Gateway
10	    AWS Config	      AWS CloudWatch	            AWS X-Ray


8. What do you understand by the term <a> 
Authentication  Authentication is the process of verifying the identity of an individual or entity to ensure that they are who they claim to be. It is a fundamental aspect of security systems and helps control access to resources, data, and services.
In summary, authentication mechanisms vary depending on the system or platform being used. While the AWS Console and API rely on username/password and access keys, respectively, SSH authentication for an Ubuntu server in AWS is accomplished using SSH key pairs. These authentication methods provide secure access control to the respective systems and help protect against unauthorized access.
</b> and describe how you authentication to the following systems;
•	AWS Console: The aws console is the web-based user interface provided by aws to manage and interact with various aws services. 
Authentication in the AWS Console is typically achieved through username and password-based authentication or by using federated identity providers such as AWS Single Sign-On. 
When logging in, users provide their AWS account credentials (username and password) or authenticate through an external identity provider if configured. Multi-Factor Authentication (MFA) can be enabled for additional layer of security. Once the credentials are verified, the user is granted access to the AWS Console based on the permissions associated with their AWS Identity and Access Management (IAM) user or role
•	AWS API: provides a comprehensive set of apis (application programming interface) to programmatically interact with aws services. 
Authentication to the AWS API is typically performed using an access key and secret access key. 
To authenticate, an application or script must include these credentials in API requests, either as query parameters or in the request headers. 
Access keys and secret access keys can be generated in the AWS Management Console for an IAM user or IAM role, and proper IAM policies should be configured to control the API actions that can be performed.
•	An ubuntu server running in AWS using ssh keys: when connecting to an Ubuntu server running in AWS using SSH (Secure Shell), authentication is achieved through SSH key pairs. 
To establish a connection, the user's SSH public key must be added to the ~/.ssh/authorized_keys file on the Ubuntu server. 
When connecting to the server, the user's SSH client uses the private key to authenticate with the server. If the private key matches the public key stored on the server, the authentication is successful, and access is granted.

9.	What do you understand by the term Authorisation and describe how you might set up authorisation to the following systems. 

  
9. What do you understand by the term <a> 
Authorisation Ans: Authorization is the process pf granting or deny access to specific resources or actions based on the authenticated user’s permissions and privilege’s it ensures that that users can only access the resources they can authorized to
</b> and describe how you might set up authorisation to the following systems;
IAM allows you to create and manage users, groups, and roles, and assign permissions to them.
To set up authorization, you can create IAM policies that define the specific actions and resources a user or group can access.
These policies can be attached to IAM users, groups, or roles, providing fine-grained control over the permissions granted.
By assigning appropriate IAM policies, you can restrict access to certain AWS services, limit actions within those services, and define resource-level permissions.
1.	AWS API:
•	Authorization in the AWS API is also managed through IAM.
•	When making API requests, the IAM policies associated with the access key being used are evaluated to determine whether the user or role has the necessary permissions.
•	IAM policies can be created to grant or deny access to specific AWS API actions, resources, and services.
•	By carefully crafting IAM policies and attaching them to the appropriate IAM users, groups, or roles, you can control the actions users can perform through the API.
2.	An AWS Linux server:
•	Authorization on an AWS Linux server is typically achieved through the use of Linux user accounts, groups, and file system permissions.
•	By default, AWS Linux instances provide an initial administrative user called "ec2-user" with sudo privileges.
•	To set up authorization, you can create additional user accounts and assign them to specific groups with appropriate permissions.
•	File system permissions can be set using commands like chmod and chown, allowing you to control read, write, and execute access to files and directories.
•	Additionally, you can leverage Linux's file system access control lists (ACLs) for more granular access control.
It's important to follow the principle of least privilege when setting up authorization. This means granting users only the permissions necessary to perform their required tasks, minimizing the risk of accidental or intentional misuse of resources.
In summary, authorization in AWS Console and API is managed through IAM policies, while on an AWS Linux server, it is achieved through Linux user accounts, groups, and file system permissions. By carefully configuring and managing these authorization mechanisms, you can enforce access control and ensure that users have appropriate permissions to perform their intended actions.


10.	Explain what these two AWSCLI commands do. What could you say about the relation between a security group and an EC2 instance?
1	aws ec2 create-security-group --group-name MySecurityGroup --description "My security group" --vpc-id vpc-1a2b3c4d

Ans: The command aws ec2 create-security-group is used to create a new security group in Amazon EC2. The provided options in the command specify the details of the security group being created:
•	--group-name MySecurityGroup sets the name of the security group to "MySecurityGroup".
•	--description "My security group" provides a description for the security group.
•	--vpc-id vpc-1a2b3c4d specifies the ID of the VPC (Virtual Private Cloud) in which the security group will be created.
The command essentially creates a new security group with the specified name, description, and associated VPC.

2 aws ec2 modify-network-interface-attribute --network-interface-id eni-686ea200 --attachment AttachmentId=eni-attach-43348162,DeleteOnTermination=false
2	Ans: The command aws ec2 modify-network-interface-attribute is used to modify the attributes of a network interface in Amazon EC2. The provided options in the command specify the modifications to be made:
•	--network-interface-id eni-686ea200 specifies the ID of the network interface to be modified.
•	--attachment AttachmentId=eni-attach-43348162,DeleteOnTermination=false modifies the attachment attribute of the network interface.
•	AttachmentId=eni-attach-43348162 specifies the ID of the attachment to modify.
•	DeleteOnTermination=false ensures that the network interface is not deleted when the EC2 instance it is attached to is terminated.

The command allows for the modification of specific attributes of a network interface, in this case, the attachment attribute to prevent automatic deletion of the network interface upon instance termination.
Relation between a security group and an EC2 instance: In Amazon EC2, a security group acts as a virtual firewall that controls inbound and outbound traffic for EC2 instances associated with it. Every EC2 instance is associated with one or more security groups, and a security group can be associated with multiple EC2 instances.
The security group defines the rules that allow or deny traffic to and from the associated EC2 instances. These rules specify which protocols, ports, and IP addresses are allowed to communicate with the instances. By configuring the security group, you can control network access to the EC2 instances, enhancing their security.
In the context of the provided commands, the first command creates a new security group, and the second command modifies the attachment attribute of a network interface. This modification might include changing the security groups associated with the network interface, thereby affecting the network traffic permissions for the corresponding EC2 instance.
  
## Site Reliability Engineering (SRE), Troubleshooting, Observability

1. 	Reliability: SRE focuses on ensuring the reliability and stability of systems by implementing practices such as error budgeting, service level objectives (SLOs), and error monitoring.
2.	Automation: SRE teams use automation to reduce manual toil, improve efficiency, and minimize human error. Automation tools and practices are employed for tasks like deployment, monitoring, and incident response.
3.	Monitoring and Alerting: SRE emphasizes comprehensive monitoring and alerting systems to gain visibility into system performance and quickly identify and respond to issues. Monitoring tools are used to track key metrics, generate alerts, and trigger incident response.
4.	Incident Response and Postmortems: SRE teams follow well-defined incident response processes to handle system disruptions promptly and effectively. Postmortem analysis is performed to understand the root causes of incidents and implement improvements to prevent their recurrence.


## DevOps and Agile Transformation principles and methodology

1.	Collaboration and Communication: Promoting collaboration and effective communication between development, operations, and other stakeholders to break down silos and foster shared responsibility.
2.	Continuous Integration and Delivery: Emphasizing the practice of frequent code integration, automated testing, and continuous delivery to enable rapid and reliable software releases.
3.	Infrastructure as Code: Treating infrastructure as code, using tools and practices to automate the provisioning, configuration, and management of infrastructure resources.
4.	Automated Deployment and Orchestration: Automating the deployment process and utilizing orchestration tools to streamline the deployment and configuration of software applications and infrastructure.
5.	Monitoring and Feedback: Implementing robust monitoring and feedback loops to gain insights into system behavior, identify issues, and drive continuous improvement.


## New commands logs - Enter up to ten new commands you have learnt this week

| Number      | Commands | What does it do and how might you check its effect     |
| :---        |    :----:   | :---  |
| 1  | ssh        | to generate key   |
| 2  | git check main       | to come out of branch   |
| 3  | cat       | to view content of a file   |
| 4  | XXXXXXXX       | YYYYYYYY   |
| 5  | XXXXXXXX       | YYYYYYYY   |
| 6  | XXXXXXXX       | YYYYYYYY   |
| 7  | XXXXXXXX       | YYYYYYYY   |
| 8  | XXXXXXXX       | YYYYYYYY   |
| 9  | XXXXXXXX       | YYYYYYYY   |
| 10 | XXXXXXXX       | YYYYYYYY   |

## Glossary of the week - Enter new technical words you have learnt this week and their meanings.

| Number   | Word | Meaning     |
| :---     | :----:   |  :---  |
| 1  | XXXXXXXX       | YYYYYYYY   |
| 2  | XXXXXXXX       | YYYYYYYY   |
| 3  | XXXXXXXX       | YYYYYYYY   |
| 4  | XXXXXXXX       | YYYYYYYY   |
| 5  | XXXXXXXX       | YYYYYYYY   |
| 6  | XXXXXXXX       | YYYYYYYY   |
| 7  | XXXXXXXX       | YYYYYYYY   |
| 8  | XXXXXXXX       | YYYYYYYY   |
| 9  | XXXXXXXX       | YYYYYYYY   |
| 10 | XXXXXXXX       | YYYYYYYY   |

