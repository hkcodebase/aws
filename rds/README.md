# RDS - Relational Database Service is

- Managed service
- Continuous Backup and restore (Point in time restore)
- Monitoring Dashboards
- Read replicas for improved read performance
- Multi AZ setup for DR (disaster recovery)
- Scaling capability (Horizontal or vertical)
- Storage backed by EBS (gp2 or io1)

** Can't SSH into RDS instances

# Storage Auto Scaling
- increase RDS db size dynamically
- RDS scales automatically once it detects that you are running out of storage
- Avoid manual scaling
- set maximum storage 
- Automatically scale if :
    - Free storage is less then 10% of allocated storage
    - Low-storage lasts atleast 5 minutes
    - 6 hours have passed since last modification
- Useful for applications with unpredictable workloads
- Supports - MySQL, postgres, SQL Server, oracle, mariadb


# READ Replicas for READ scalability

- upto 15 replicas across within AZ, cross AZ or cross region
- Replication is async so Eventually consistent
- Replicas can be updated to their own DB
- Application must update connection string to leverage read replicas

# READ Replica Use cases
- Can be used to increase performance for heavy read applications
- Analytics applications can run on read replicas

# Read Replica Cost
-  No cost in same region
-  Cross region replication will incur cost

# READ Replica (Disaster Recovery)
- SYNC Replication
- One DNS name - automatic app failover to standby
- increase availability
- Failover in case of loss of AZ, network, instance or storage
- No manual intervention in App
- Not used for scaling 