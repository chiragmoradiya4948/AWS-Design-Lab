# What is KMS - Key Management Service 

####AWS Key Management Service (KMS) is a managed service that makes it easy for you to create and manage keys and control the use of encryption across a wide range of AWS services. KMS is a secure and resilient service that uses FIPS 140-2 validated hardware security modules to isolate and protect your keys.

# Best use case

E-commerce websites, such websites has more traffic on discount sale compare to normal days.

# Road map
1) We use Dynamo DB service for encrypt to decrypt using multi region key.
2) We create table in n virginia and make a replica of same table in region asia pacific - Mumbai 
3) We create multi region key and same we will replicate into region asia pacific - Mumbai
4) We disble key in region asia pacific - Mumbai and check table details
5) We able key in region asia pacific - Mumbai and check table details


# End of this page
