# What is SNS

Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication.

# What is Alarms in Cloudwatch?
The new CloudWatch Alarms feature allows you to watch CloudWatch metrics and to receive notifications when the metrics fall outside of the levels (high or low thresholds) that you configure. You can attach multiple Alarms to each metric and each one can have multiple actions.

Alarms watch metrics and execute actions by publishing notifications to Amazon SNS topics or by initiating Auto Scaling actions. SNS can deliver notifications using HTTP, HTTPS, Email, or an Amazon SQS queue. Your application can receive these notifications and then act on them in any desired way.

A CloudWatch Alarm is always in one of three states: OK, ALARM, or INSUFFICIENT_DATA. When the metric is within the range that you have defined as acceptable, the Monitor is in the OK state. When it breaches a threshold it transitions to the ALARM state. If the data needed to make the decision is missing or incomplete, the monitor transitions to the INSUFFICIENT_DATA state.

# Road map

Statement : If EC2 instance' network traffic goes on more than 10k bytes, it will trigger mail to recipient.

1) Create SNS service for setting target of notification.
2) Create 


#### Step 1: Go to AWS Management console and search 'SNS', Set 'Topic name' & click on next step.
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2: On next page, select Standard & give name of SNS, click on 'Create topic'
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 3: Once topic is created click on 'Subscriptions' & 'Create Subscriptions'

####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 4: Once topic is created click on 'Subscriptions' & 'Create Subscriptions'

####
<img src="/AWS CloudWatch/Images/AWS Clou9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

Endpoint

