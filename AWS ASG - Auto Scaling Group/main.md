# What is EC2 Auto Scaling #

#### 
You can make sure that you have the appropriate number of Amazon EC2 instances available to handle the load for your application by using Amazon EC2 Auto Scaling. ASG (Auto Scaling Groups) are assemblies of EC2 instances that you build. Each Auto Scaling group has a minimum number of instances that can be specified, and Amazon EC2 Auto Scaling makes sure that your group never falls below this number.
####

####
If scaling policies are specified,then Amazon EC2 Auto Scaling can start or stop instances based on what and how demand there is for your application.
####

####
For instance, the next Auto Scaling group has a minimum instance size of one, a targeted instance capacity of two, and a maximum instance size of four. Within your minimum and maximum number of instances, the scaling policies you design change the number of instances according to the parameters you set.
####

<img src="/AWS-Design-Lab/AWS ASG - Auto Scaling Group/AWS_ASG.png" width="450px" height="350px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />

####
Your applications benefit from Amazon EC2 Auto Scaling in the following ways:
####

- Better fault tolerance: When an instance becomes unhealthy, Amazon EC2 Auto Scaling can identify it, terminate it, and run a new instance to replace it. Amazon EC2 Auto Scaling can also be configured to use different Availability Zones. If one Availability Zone fails, Amazon EC2 Auto Scaling can launch instances in another to compensate.

- Better availability: Amazon EC2 Auto Scaling ensures that your application always has enough capacity to address current traffic demands.

- Better cost management: Amazon EC2 Auto Scaling can increase and decrease capacity dynamically as needed. You save money by creating instances when they are needed and terminating them when they aren't since you pay for the EC2 instances you utilise.


####
Best use case
####
- ecommerce website, such websites has more traffic on discount sale compare to normal days.

#### Road map ####

1) Plan to have minimum & maximum instances & desire capacity for your setup.
2) Configure load balancer.
3) Create number of instance as per set matrix.
4) Configure auto scaling group that specify a launch template that contains settings common to all EC2 instances that are launched by this Auto Scaling group. 
5)

Attach to an existing load balancer
Choose from your existing load balancers.

#### Implementation on lab ####

####

<img src="/AWS-Design-Lab/AWS ASG - Auto Scaling Group/Images/AWS ASG 00001.png" width="450px" height="350px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
####
<img src="/AWS-Design-Lab/AWS ASG - Auto Scaling Group/Images/AWS ASG 00001.png" width="450px" height="350px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  

