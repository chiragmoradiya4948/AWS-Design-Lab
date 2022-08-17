# What is RDS
Amazon RDS provides scalable relational database capacity at a low cost while automating time-consuming administration tasks like hardware provisioning, database setup, patching, and backups. It frees you up to focus on your applications, allowing you to provide them with the high availability, security, and compatibility they require.

# Benefits and Features
1) Easy to Administer: 
Amazon RDS makes it easy to go from project conception to deployment. Access the capabilities of a production-ready relational database in minutes. No need for infrastructure provisioning, and no need for installing and maintaining database software.
2) Available and Durable:
Amazon RDS lets you deploy a database across multiple Availability Zones and automatically fails over to a standby instance in case of an outage. Amazon RDS has many other features that enhance reliability for critical production databases, including automated backups, database snapshots, and host replacements.
3) Highly Scalable:
You can scale your database's compute and storage resources with only a few mouse clicks or an API call, often with no downtime. Many Amazon RDS engine types allow you to launch one or more Read Replicas to offload read traffic from your primary database instance.
4) Fast:
Amazon RDS supports the most demanding database applications. You can choose between two SSD-backed storage options: one optimized for high-performance OLTP applications, and the other for cost-effective general-purpose use.

# Use cases
- Web and Mobile Applications, Ecommerce Applications

# Road Map
1) We create dababase in region 'Mumbai'
2) We create snapshot of database
3) We copy snapshot into another region & re-configure database as per our requirment
5) We use that same database into new region, by restoring snapshot of database

# implementation on lab

#### Step 1 : Search 'RDS' in search bar and click on create database, select 'Standard create' &  MySQL as engine options. 
####
<img src="/AWS RDS - Migration/images/AWS RDS 1.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 2 : Select 'free tier' as per below
####
<img src="/AWS RDS - Migration/images/AWS RDS 2.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 3 : Select other options as per below
####
<img src="/AWS RDS - Migration/images/AWS RDS 3.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####
####
<img src="/AWS RDS - Migration/images/AWS RDS 3(1).png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 4 : Set other fields by default as it is and click on submit. It will take some time to create database.
####
<img src="/AWS RDS - Migration/images/AWS RDS 4.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 5 : Once database is 'active', click on action and 'Take Snapshot'.
####
<img src="/AWS RDS - Migration/images/AWS RDS 5.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 6 : Set Database name and Snapshot name, click on 'Take a snapshot'. It will take some time to create a snapshot.
####
<img src="/AWS RDS - Migration/images/AWS RDS 7.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 7 : Once snapshot created, click on 'Copy snapshot'
####
<img src="/AWS RDS - Migration/images/AWS RDS 8.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 7 : It will ask for destination region where need to create same database.
####
<img src="/AWS RDS - Migration/images/AWS RDS 9.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 8 : If you open RDS/Snapshot on destination region, you will see copy of snapshot.
####
<img src="/AWS RDS - Migration/images/AWS RDS 10.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####

#### Step 9 : You can create database from snapshot by simply 'restore snapshot'
####
<img src="/AWS RDS - Migration/images/AWS RDS 11.png" width="auto" height="auto" style="border:5px double black;"
     alt="Application Load Balancer"
     style="float: left; margin-right: 6px;" />
####


 ## End of page ##
 
