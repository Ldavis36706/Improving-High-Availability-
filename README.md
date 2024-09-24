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
</b> 

<h2>Program walk-through:</h2>

<p align="center">

Create a launch template:
 <br/>
![Launch Template Successful](https://github.com/user-attachments/assets/3ce5c01e-b5a0-4603-b9d4-1038531ea41f)

<br />

Create an auto-scaling group:
 <br/>
![Successful Auto Scaling Group](https://github.com/user-attachments/assets/5e0e6e66-d97f-4be9-9c0c-725d9d5f0599)


<br />

Test auto-scaling group by terminating an instance:
 <br/>
![Terminate Instance](https://github.com/user-attachments/assets/eac70203-b18c-4520-9c6d-a7bc5664b58a)


<br />

Check to see if a replacement instance was launched:
 <br/>
![New Instance Created after first stopped](https://github.com/user-attachments/assets/50a5c23a-b4af-48d5-aa1c-a997da43dd12)

<h2>Summary</h2>
The application was running on two Amazon EC2 instances, but both instances were hosted in a single Availability Zone. This setup presented a risk of downtime if the Availability Zone experienced any issues, compromising the application's high availability. To improve the resilience of the application, I needed to redesign the architecture by distributing the EC2 instances across multiple Availability Zones. This required implementing an Auto Scaling group and ensuring the instances could scale automatically based on traffic demand, while maintaining load distribution with a Network Load Balancer. I started by creating a launch template to standardize the EC2 instance configuration, including the Amazon Machine Image (AMI) and instance type. Next, I set up an Auto Scaling group that extended the instances across multiple Availability Zones, defining minimum and maximum instance limits for optimal scaling. I then integrated the Auto Scaling group with a Network Load Balancer to efficiently distribute incoming traffic across all running instances. Finally, I monitored the system using AWS CloudWatch to verify the scaling activities and instance health. By implementing these changes, I enhanced the application's high availability and fault tolerance. The Auto Scaling group ensured that instances could be automatically launched or terminated based on demand, and the Network Load Balancer distributed traffic effectively. This architecture minimized downtime risks and optimized resource usage, making the system more resilient to potential failures.
<br />



