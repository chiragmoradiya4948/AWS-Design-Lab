# Authenticating to RDS MySQL using Kerberos and Active Directory

When users connect to MySQL DB instance, you can use Kerberos authentication to authenticate them. To enable Kerberos authentication, the DB instance collaborates with AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD). Authentication requests are forwarded when users authenticate with a MySQL DB instance that is a member of the trusting domain. Forwarded requests are routed to the domain directory created with AWS Directory Service.

It can save you time and effort to keep all of your credentials in the same directory. This method provides a centralised location for storing and managing credentials for multiple DB instances. Using a directory can also boost your overall security.

# What is Kerberos?

# What is RDS?

# What is Active Directory?

# Road Map

1) AWS Managed Microsoft AD a prerequisite
2) RDS MySQL instance should be domain joined.
3) Authentication requests are forwarded to AD.


