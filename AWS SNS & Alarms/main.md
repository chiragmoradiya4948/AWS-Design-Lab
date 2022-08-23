# What is SNS

Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication.

# What is Alarms in Cloudwatch?
The new CloudWatch Alarms feature allows you to watch CloudWatch metrics and to receive notifications when the metrics fall outside of the levels (high or low thresholds) that you configure. You can attach multiple Alarms to each metric and each one can have multiple actions.

Alarms watch metrics and execute actions by publishing notifications to Amazon SNS topics or by initiating Auto Scaling actions. SNS can deliver notifications using HTTP, HTTPS, Email, or an Amazon SQS queue. Your application can receive these notifications and then act on them in any desired way.

A CloudWatch Alarm is always in one of three states: OK, ALARM, or INSUFFICIENT_DATA. When the metric is within the range that you have defined as acceptable, the Monitor is in the OK state. When it breaches a threshold it transitions to the ALARM state. If the data needed to make the decision is missing or incomplete, the monitor transitions to the INSUFFICIENT_DATA state.

# Road map

Statement : If EC2 instance' network traffic goes on more than 10k Bytes, it will trigger mail to recipient.

1) Create SNS service for setting target of notification.
2) Create 


#### Step 1: Go to AWS Management console and search 'SNS', Set 'Topic name' & click on next step.
####
<img src="/AWS SNS & Alarms/Images/1.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2: On next page, select Standard & give name of SNS, click on 'Create topic'
####
<img src="/AWS SNS & Alarms/Images/2.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 3: Once topic is created click on 'Subscriptions' & 'Create Subscriptions'

####
<img src="/AWS SNS & Alarms/Images/3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 4: On next page, Select 'Email' as protocol and endpoint as your mail address, click on Create Subscriptions.

####
<img src="/AWS SNS & Alarms/Images/4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####


#### Step 5: Once Subscriptions is created, status is showing 'Pending confirmation', You need to confirm mail from your inbox.

####
<img src="/AWS SNS & Alarms/Images/5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 6: once you confirm, you will see status is 'Confirmed'

####
<img src="/AWS SNS & Alarms/Images/6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

# Now SNS is created with target, After that you can launch any EC2 instance for next steps.

#### Step 7: Go to AWS Management console and search 'Cloudwatch', go to Alarms & click on 'Create a alarm.

####
<img src="/AWS SNS & Alarms/Images/7.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 8: On next page, Select metric and follow EC2> Pre-instance Metrics > NetworkIn as Metric name (use instance name)

####
<img src="/AWS SNS & Alarms/Images/8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####


#### Step 9: Once you select metric, and click on next you will see screen like below.

####
<img src="/AWS SNS & Alarms/Images/9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####


#### Step 10: Set condition as 'Static' in Threshold type and 10000as values.

####
<img src="/AWS SNS & Alarms/Images/10.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 11: Click on next page, set notification as per below.

####
<img src="/AWS SNS & Alarms/Images/11.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 11: You can see Alarm is set, see graph of network traffic.

####
<img src="/AWS SNS & Alarms/Images/12.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 11: You will get mail as per below, when network traffic go beyong the 10k Bytes

####
<img src="/AWS SNS & Alarms/Images/13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
## End of page ## 

