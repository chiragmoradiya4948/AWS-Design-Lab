# What is AWS image builder
EC2 Image Builder is a fully managed service that makes it simple to create, customise, and deploy OS images without the need for scripting.

# How it works

####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 1.png" width="650px" height="400px" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

# Use cases  
1) Automate build and maintenance of images 
2) Increase image quality with automated validation 
3) Enforce consistent policies in heterogeneous environments

# Benefits
1) Improve IT productivity:
2) Produce secure and up-to-date images
3) Simple image management for both AWS and on-premises
4) Built-in support for validation

Create image pipeline

### Implementation on lab ###

#### Step 1 : Go to AWS image builder > Click on 'Create image pipeline'.
The image pipeline in Image Builder defines all aspects of the process to customize images. It consists of the image recipe, infrastructure configuration, distribution, and test settings.


#### Step 2 : Set Pipeline name and select 'manual' as build schedule
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 2.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 3 : Click on 'Create new recipe & Image type as 'AMI'
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 4 : Select build components as amazon-corretto-11-headless & aws-cli-version-2-linux.
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 5 : Select Image name as Amazon Linux 2 x86
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 7.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 6 : Now on next page Click on 'Create a new infra configuration' and create role, go to IAM > Roles > Create role, and set as per below
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 7 : Now on next page, This instance role is configured using the 
EC2InstanceProfileForImageBuilder, 
EC2InstanceProfileForImageBuilderECRContainerBuilds, and 
AmazonSSMManagedInstanceCore managed policy. And set Role name.
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 8 : Select newly created role on 'IAM role'
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 10.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 9 : Select 't2.micro' as instance type and click on next
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 11.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 10 : Set 'Create distribution setting using service defaults' and click on submit.
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 12.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 11 : Pipeline is created, now need to run pipeline, so click on 'Run pipeline'
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 12 : Pipeline status is 'Building'.
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 14.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 13 : Now go to EC2 instance dashboard, can see our newly creatd pipeline tested & built automatically by AWS
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 15.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 14 : Pipeline status is showing like 'Distributing' > 'Integrating' > 'Active'
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 16.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 15 : now our OS image is created, go to EC2 dashboard >. launch EC2 & select our AMI from My AMIs.
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 18.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 16 : Set other configurations and create instance, once instance is created, connect to EC2 instance and see java vestion, you can see Corretto is installed.
####
<img src="/AWS EC2 Image Builder/Images/AWS Image builder 19.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

# End of page #
