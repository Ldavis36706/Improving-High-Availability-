<h1> Improving High Availability with Auto Scaling and Network Load Balancer in AWS
</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
In this project, I addressed a problem related to increasing the high availability of an application running on Amazon EC2 instances behind a Network Load Balancer (NLB). Initially, the architecture consisted of two EC2 instances located in a single Availability Zone, which made the system vulnerable to downtime if the zone failed. To improve availability, I implemented an Auto Scaling group that extended the EC2 instances across multiple Availability Zones. The Auto Scaling group was connected to the NLB, ensuring automatic scaling and fault tolerance for the application.
<br />

<h2>Languages and Utilities Used</h2>

- <b>AWS Management Console: The primary utility for creating and managing resources like EC2 instances, Launch Templates, Auto Scaling groups, and Load Balancers.</b> 
- <b>EC2 (Elastic Compute Cloud) : For hosting and managing virtual servers (EC2 instances).</b>
- <b>Amazon EC2 Auto Scaling: Automatically adjusts the number of EC2 instances in response to changing demand.</b> 
- <b>Amazon VPC (Virtual Private Cloud): For networking, where you configured subnets and availability zones.</b>
- <b>AWS CloudWatch: For monitoring and collecting Auto Scaling metrics.</b> 
- <b>Network Load Balancer: Used to distribute incoming traffic among EC2 instances across multiple Availability Zones.</b>
- <b>Security Groups: For configuring network-level security (firewalls) for EC2 instances.</b> 

<h2>Environments Used </h2>

- <b>Cloud Platform:
•	AWS (Amazon Web Services): This project was conducted entirely in AWS, utilizing several of its services.
</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">

Creating a launch template: <br/>
![Launch Template Successful](https://github.com/user-attachments/assets/3ce5c01e-b5a0-4603-b9d4-1038531ea41f)

<br />
