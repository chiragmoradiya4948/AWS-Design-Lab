# Authenticating to RDS MySQL using Kerberos and Active Directory

When users connect to MySQL DB instance, you can use Kerberos authentication to authenticate them. To enable Kerberos authentication, the DB instance collaborates with AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD). Authentication requests are forwarded when users authenticate with a MySQL DB instance that is a member of the trusting domain. Forwarded requests are routed to the domain directory created with AWS Directory Service.

It can save you time and effort to keep all of your credentials in the same directory. This method provides a centralised location for storing and managing credentials for multiple DB instances. Using a directory can also boost your overall security.

# What is Kerberos?

# What is RDS?

# What is Active Directory?

# Road map

1) AWS Managed Microsoft AD a prerequisite
2) RDS MySQL instance should be domain joined.
3) Authentication requests are forwarded to AD.

# Implementation steps

1) Create an AWS Managed Microsoft AD
2) Create a new AD user
3) Create a new RDS MySQL instance and join to the AD
4) Create a user with external authentication on RDS MySQL
5) Connect to the server using the AD user


#### Step 1: Go to AWS Management console and search 'Directory Service', Click on 'set up directory'.
####
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 1.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2: Select 'AWS Managed Microsoft AD', then click on next.
####
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 2.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 3: Click on 'Standard Edition' Set Directory DNS name (Domain Name) & Admin password, Click on next page
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 4: On Networking field, leave VPC setting as it is,Click on next page
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 5: Review all steps and click on 'Create Directory'.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

## Directory is created, now we will create Windows machine, which is part of this domain.

#### Step 6: Go to EC2 dashboard, click on launch instance, and select as per below window OS.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 7: On Advanced setting, select newly created directory in 'Domain join category'.
Notes : Please create Key pair, so that you can recover windows password or set new password for windows instance.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 7.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 8: Once instance is created, get connected via RDP,  
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 9: We need to install AD in windows machine, so go to > Server management > tools > add roles and features > select as per below and install AD.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####


#### Step 10: Once Active Directory is created, create a user 'rdsuser'.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

## Upto this point, Windows AD is also created, now we configure RDS with 

#### Step 11: Search 'RDS', click on create a database, and set as per below.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 12: Select 'Free tier' from template option and set DB instance identifier, master username, password.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 14.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 13: Select Password & keyberos authentication and select created directory, Click on 'Create database'
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 15.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

Now RDS database is also configured with AD & Keyberos authentication.

#### Step 14: Connect your RDS instance with your any of instance within VPC, & auth with root user.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 10.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 15: Now Connect to the server using the AD user (rdsuser), it will authenticated via Keyberos.
#### 
<img src="/AWS - RDS MySQL Auth using Kerberos and AD/Images/AWS KB 11.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

# End of page #
