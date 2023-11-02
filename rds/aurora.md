# Amazon Aurora

- AWS managed database service 
- Aurora is cloud optimized 
- automatically grows in increment of 10 GB upto 128 GB 
- It is proprietary technoligy from AWS (not open sourced)
- Aurora can have upto 15 replicas and the replication process is faster then MySQL
- Failover in Aurora is instantaneous. it is High available native.



---
- 6 copies over 3 AZ out of which:
- 4 are for write
- 3 are for read
- Self healing with peer to peer replication
- Storage is striped oves 100s of volumes
- Automatic failover for master in less than 30 seconds
Shared storage volume provides Replication + Self healing + Auto Expanding
- Replicas support cross region replication

---

## Features of Aurora

- Automatic Failover
- Backup and recovery
- Isolation and security
- Industry compliance
- Push-button scaling
- Automatic patching with zero downtime
- Advanced Monitoring
- Routine Maintenance
- Backtrack - restore data at any given point of time without using backups

## RDS and Aurora Security

- At Rest Encryption - must be defined at launch time
  - Encryption using AWS KMS
  - If master is not encrypted then Read replicas will not be encrypted
- In-flight encryption: TLS-ready by default, use the AWS TLS root certificates client side.
- IAM Authentication: IAM Roles to connect to your database
- Security Groups - control network access to your RDS/Aurora DB
- No SSH Available except on RDS Custom
- Audit logs can be enabled and sent to cloudwatch logs for longer retention
