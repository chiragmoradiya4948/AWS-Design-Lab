# AWS ELB #

#### What is ELB used for ####

#### Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs). ####

##### 
Your incoming traffic is automatically split among numerous targets, including EC2 instances, containers, and IP addresses in one or more Availability Zones, thanks to elastic load balancing. It keeps track of the health of the registered targets, only sending traffic to those that are in good shape. As the volume of incoming traffic changes over time, elastic load balancing scales your load balancer. The great majority of workloads can be handled by it automatically scaling 
#####

#### Supported ELB ###
- Classic Load Balancer (CLB) – this is the oldest of the three and provides basic load balancing at both layer 4 and layer 7.
- Application Load Balancer (ALB) – layer 7 load balancer that routes connections based on the content of the request.
- Network Load Balancer (NLB) – layer 4 load balancer that routes connections based on IP protocol data.
- Gateway Load Balancer (GLB) – layer 3/4 load balancer used in front of virtual appliances such as firewalls and IDS/IPS systems.


##### The load balancer type that best meets your demands can be chosen. In this manual, application load balancers are covered. #####

<img src="/Apps_ELB.png" width="250px" height="250px"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />

#### Now let's create application load balancer here ####

#### Road map ####
1) To begin, we create 2 instances in various regions (Must be listening on HTTP : 80).
2) On both instances, we host the same static website.
3) We configure application load balancer.
4) Verify the health of both instances.
5) Use an both IP address to test a website.
6) By examining each instance's response individually, we can see how the load balancer works.
7) We purposefully removed one instance (Failed over).
8) AWS ELB checks the instance's status.
9) We have to hear a response from a different instance.

#### implementation on lab ####


#### And in this way, we can see that if one of our instances fails to start, all of our traffic will instantly switch to a healthy server.####

# End page #
