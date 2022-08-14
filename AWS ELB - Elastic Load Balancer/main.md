# AWS ELB #

#### What is ELB used for ####

#### Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs). ####

##### 
Your incoming traffic is automatically split among numerous targets, including EC2 instances, containers, and IP addresses in one or more Availability Zones, thanks to elastic load balancing. It keeps track of the health of the registered targets, only sending traffic to those that are in good shape. As the volume of incoming traffic changes over time, elastic load balancing scales your load balancer. The great majority of workloads can be handled by it automatically scaling 
#####

#### Supported ELB ###
- Application load balancers
- Network load balancers 
- Gateway load balancers, and classic load balancers


##### The load balancer type that best meets your demands can be chosen. In this manual, application load balancers are covered. #####

<img src="/AWS ELB - Elastic Load Balancer/Apps_ELB.png" width="250px" height="250px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />

#### Road map ####

1) We create 2 linux instances in same region (I have installed httpd.service & add Hello World script).
2) We create load balacer and pointing out newly created security group which has target of these 2 instance.
3) Once load balancer is created, we access load balancer IP/DNS on browser.
4) We can see while refreshing page get alternative response from both the instances.
5) We purposefully shutdown one instance,then we get only one response from instance.
6) Because our load balancer will automatically detect one unhealthy instance and transter all HTTP requests to only healthy instance.

### Implementation on lab ###

#### Step 1 & 2 : Go to EC2 > Auto scaling group, Enter name of ASG & Click on 'Create a launch template'
####
<img src="/AWS ASG - Auto Scaling Group/Images/AWS ASG 00001.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

     
