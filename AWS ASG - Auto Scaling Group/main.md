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

<img src="/AWS ASG - Auto Scaling Group/AWS_ASG.png" width="450px" height="350px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />

####
Your applications benefit from Amazon EC2 Auto Scaling in the following ways:
####

- Better fault tolerance: When an instance becomes unhealthy, Amazon EC2 Auto Scaling can identify it, terminate it, and run a new instance to replace it. Amazon EC2 Auto Scaling can also be configured to use different Availability Zones. If one Availability Zone fails, Amazon EC2 Auto Scaling can launch instances in another to compensate.

- Better availability: Amazon EC2 Auto Scaling ensures that your application always has enough capacity to address current traffic demands.

- Better cost management: Amazon EC2 Auto Scaling can increase and decrease capacity dynamically as needed. You save money by creating instances when they are needed and terminating them when they aren't since you pay for the EC2 instances you utilise.


#### Best use case
- E-commerce websites, such websites has more traffic on discount sale compare to normal days.

#### Road map ####

1) Think about having a minimum and maximum number of instances and desired capacity for your installation.
2) Set up the load balancer.
3) Create an auto scaling group and define a launch template that contains settings that are shared by all EC2 instances launched by this Auto Scaling group.
5) Attach to an existing load balancer.
6) Determine the availability zone in which instances will be produced during auto scaling.
7) Once the ASG has been built, examine the EC2 instances that are currently running.
8) Purposefully stop One instance
9) ASG will create a new instance, that you can see on the EC2 instance.

### Implementation on lab ###

#### Step 1 & 2 : Go to EC2 > Auto scaling group, Enter name of ASG & Click on 'Create a launch template'
####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00001.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 3 & 4 : Enter template name and description & rest setting by default as you can see on right side summary window
####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00002.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 5 : Go back to ASG page and select newly created template, click on next
####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00003.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 6 & 7 : On network configure page, choose availability zone where you want to instanced to be configured
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00004.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   
   #### Step 8 : On next page click on 'ELB', it will check ELB health regularly along with EC2 health
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00005.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 9 & 10 : Sext matrix for group size & rest setting by default, And review the ASG and click on 'create it'
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00006.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 11 : It will take some time and after that you can see ASG is created 
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00007.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####
   #### Step 12 : If you expand it, you will see 2 instances (As per desired instance) are running on 'Instance management' tab
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00008.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 13 : You can also see running instances on EC2 dashboard, Now we purposefully stop instance 'i-0638f89a23db1829f'
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00009.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00010.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 14,15 & 16 : Now ASG group automatically detects 'unhealthy' instance and will create new instance on set availability zone
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00011.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
   #### Step 17 : Newly created instance can see on EC2 dashboard with running state
   ####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00012.png" width="auto" height="auto"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
   ####  
  
  ## End of page ##
