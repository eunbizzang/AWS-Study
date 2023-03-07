RDS Read Replicas for read scalability

- Up to 5 Read Replicas
- Within AZ, Cross AZ or Cross Region
- Replication is ASYNC, so reads are eventually consistent
- Replicas can be promoted to their own DB
- Applications must update the connection string to leverage read replicas

RDS Read Replicas – Use Cases
- You have a production database that is taking on normal load
- You want to run a reporting application to run some analytics
- You create a Read Replica to run the new workload there
- The production application is unaffected
- Read replicas are used for SELECT(=read) only kind of statements(not INSERT, UPDATE, DELETE)

RDS Read Replicas – Network Cost
- In AWS there’s a network cost when data goes from one AZ to another
- For RDS Read Replicas within the same region, you don’t pay that fee

RDS Multi AZ (Disaster Recovery)
- SYNC replication
- One DNS name – automatic app
failover to standby
- Increase availability
- Failover in case of loss of AZ, loss of
network, instance or storage failure
- No manual intervention in apps
- Not used for scaling
- Multi-AZ replication is free
- Note:The Read Replicas be setup as
Multi AZ for Disaster Recovery (DR)

RDS – From Single-AZ to Multi-AZ
- Zero downtime operation (no
need to stop the DB)
- Just click on “modify” for the
database
- The following happens internally:
- A snapshot is taken
- A new DB is restored from the
snapshot in a new AZ
- Synchronization is established
between the two databases

Managed Oracle and Microsoft SQL Server Database with OS and
database customization
• RDS: Automates setup, operation, and scaling of database in AWS
• Custom: access to the underlying database and OS so you can
• Configure settings
• Install patches
• Enable native features
• Access the underlying EC2 Instance using SSH or SSM Session Manager
• De-activate Automation Mode to perform your customization, better to take a DB snapshot before
• RDS vs. RDS Custom
• RDS: entire database and the OS to be managed by AWS
• RDS Custom: full admin access to the underlying OS and the database