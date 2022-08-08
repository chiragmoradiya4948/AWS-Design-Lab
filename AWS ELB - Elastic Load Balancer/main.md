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

<img src="/Apps_ELB.png" width="250px" height="250px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />

#### Now let's create application load balancer here ####


#### Road map ####
- First we create 2 instances from different regions (Must be listening on HTTP : 80).
- We host (Same) static website on both instances.
- We configure application load balancer.
- Check both instance's health status.
- Test website by accessing IP.
- We can see how load balacer works by checking response from both instance one by one.
- We purposefully down one instance (Failed over).
- AWS ELB checks status of instance.
- We must get response from another instance.


#### And this is how we can see that if one of our instance failed to starts, automatically our traffic foes to another healthy server ####

# End page #
     
