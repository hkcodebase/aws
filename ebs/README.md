# EBS - Elastic Block Store

#### About EBS Volumes
- EBS Volumes are instance storage that can be attached to EC2 Instances
- EBS Volumes are Network Drive (not a physical drive)
- EBS Volumes are Locked to an AZ*.
- EBS Volumes can be attached to any instance in an AZ*.
- EBS Volumes can be attached to a single instance
- A single EC2 Instance can have multiple EBS Volumes and one of them will be root volume
- EBS Volume can be deleted on EC2 instance termination by selecting attribute delete on termination.
- Root EBS volume by default is selected to delete on ec2 instance termination.

#### EBS Snapshots
- Snapshots are backup of your EBS volumes at a point of time
- Snapshots can be copied and moved to another AZ
- Snapshots can be restored to create a copy of EBS Volume.

*AZ - Availabilty Zone

#### [Know More about EBS Here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)
