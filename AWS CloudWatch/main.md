# What is CloudWatch

Amazon CloudWatch is an accuracy and monitoring service designed for DevOps engineers, developers, site reliability engineers (SREs), IT managers, and product owners. CloudWatch provides data and actionable insights to help you monitor your applications, respond to changes in system performance, and optimise resource utilisation. Logs, metrics, and events are used by CloudWatch to collect monitoring and operational data. You gain complete visibility of your AWS resources, applications, and services running on AWS and on-premises, as well as a unified view of operational health. To keep your applications running smoothly, you can use CloudWatch to detect anomalous behaviour in your environments, set alarms, visualise logs and metrics side by side, take automated actions, troubleshoot issues, and discover insights.

# Benefits 
1) Use a single platform for observability  
2) Collect metrics on AWS and on premises 
3) Improve operational performance and resource optimization 
4) Get operational visibility and insight

# How it works
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

# Road map

Statement : Create log groups for lambda function with Python scripts.

1) Create Python scripts with lambda function.
2) Deploy & run Python code.
3) Create Cloudwatch' log groups for lambda function.
4) Make changes on Python script and see cloudwatch's log groups.


#### Step 1: Go to AWS Management console and search 'Lambda', Click on 'Create function', & select as per below.
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2: Once lambda function is created, you can see python code as per below, You can test & run the code.
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 1.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

## Now lambda function is created, we will create log groups ##
Notes : Many of time, log group is automatically created for lambda function, so don't need to create log groups.

#### Step 3: Go to AWS Management console and search 'Cloudwatch', Click on 'Log groups', & you will see lambda function log group there.
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 2.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 4: Now go back to lambda function and make some changes on code, deply and run the code
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 5: Click on 'log group' & log streams, you will see recent streams.
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 6: Click on recent log streams, you will error on log streams.
####
<img src="/AWS CloudWatch/Images/AWS Cloudwatch 5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

## End of page ##
