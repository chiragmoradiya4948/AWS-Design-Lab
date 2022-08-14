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


##### The load balancer type that best meets your demands can be chosen. In this tutorial, application load balancers are covered. #####

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

#### Step 1 : Go to EC2 > Launch Instances & create 2 linux instances
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 1.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2 : Open load balancer console and create load balancer with below settings.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####     

#### Step 3 : In Security groups, click on 'Create new security group' & set as per below parameters.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####      

#### Step 4 : In Listeners and routing, click on 'CCreate target group' & select 'Instances', click on next
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####   

#### Step 5 : Now select both instances, because we need to use both instances for requests handling, click on Include as pending below, and next
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####   

#### Step 6 : You can see Target Group is created.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####   

#### Step 7 : Go back to load balancer console and refresh, select newly created 'Target Group'
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 8 : Review details as per below.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 9 : Now load balacer is created and active. We access our application with load balancer's DNS/IP.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 10 : Now load balacer is created and active. We access our application with load balancer's DNS/IP.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 10 : When we hit DNS for first time, we get below response from linux_first_server.
####
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 11 : However we we hit refresh button,then we get response from linux_second_server. It means we have set load balancer correctly.
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 12 : We purposefully shutdown, linux_first_server.
<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

#### Step 13 : Now when we hit load balancer's DNS on browser and repeatedly refresh we only get response from linux_second_server. Because our load balancer will automatically detect one unhealthy instance and transter all HTTP requests to only healthy instance. 

<img src="/AWS ELB - Elastic Load Balancer/images/AWS ELB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
#### 

### End of page ###
