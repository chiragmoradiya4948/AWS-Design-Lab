# What is KMS - Key Management Service 

#### AWS Key Management Service (KMS) is a managed service that makes it easy for you to create and manage keys and control the use of encryption across a wide range of AWS services. KMS is a secure and resilient service that uses FIPS 140-2 validated hardware security modules to isolate and protect your keys.

# Road map
1) We use Dynamo DB service for encrypt to decrypt using multi region key.
2) We create table in 'n virginia' and make a replica of same table in region 'asia pacific - Mumbai'.
3) We create multi region key and same we will replicate into region 'asia pacific - Mumbai'.
4) We disble key in region 'asia pacific - Mumbai' and check table details
5) We enable key in region 'asia pacific - Mumbai' and check table details

### Implementation on lab ###

#### Step 1: We will create Dynamo DB table by giving Table name and Partition key.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 1.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2: We can add items on employee_data table
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 2.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 3: EMS console, we will create Symmetric key in multi region and click on next
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 4: We can set Alias & description of key and click on next.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 5: We can rest setting by default as it is and submit for key
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 6: We can create replica of this key into region mumbai
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 6.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
     
#### 
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 7.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

####
#### Step 7: We open Dynamo DB service click on Additional settings and scroll down.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 10.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 8: Click on 'manage encryption and On next page set as per below.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 9: We can see Key is set for Dynamo DB service.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 10: We set disable this key in region mumbai and can check whether we can see items on dynamo DB or not.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 11.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 11: We get error as KMS key disabled
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 12.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 12: We again go to key and make it enabled
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 13.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
#### Step 13: you can see now we can see items on table in Mumbai (Multi) region.
####
<img src="/AWS KMS - Key Management Service/images/AWS KMS - 14.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

# End of this page
