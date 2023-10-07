# EC2 - Elastic Cloud Compute

## [About EC2](https://aws.amazon.com/ec2/)
## [EC2 instance types](https://aws.amazon.com/ec2/instance-types/)
## [Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/security-groups.html)
## [Create EC2 Instance and Connect via SSH](https://hkcodeblogs.medium.com/aws-ec2-create-and-connect-to-instance-via-ssh-354a0c1909f)

## [AMI - Amazon Machine Image](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)
![](./ami.png)

- AMI are image of an EC2 Instance at a point of time contains software, configuration or packages

## EC2 can be launched via - 
  - AWS Provided AMI
  - User AMI
  - AWS Marketplace AMI 

## AMI Create Option
![](./ami_create_option.png)

## EC2 Storage Options
 - [EBS - Elastic Block Store](./ebs/README.md)

    - EBS Volumes are instance storage that can be attached to EC2 Instances
    - EBS Volumes are Network Drive (not a physical drive)
    - EBS Volumes are Locked to an AZ*.
    - EBS Volumes can be attached to any instance in an AZ*.
    - EBS Volumes can be attached to a single instance
    - A single EC2 Instance can have multiple EBS Volumes and one of them will be root volume
    - EBS Volume can be deleted on EC2 instance termination by selecting attribute delete on termination.
    - Root EBS volume by default is selected to delete on ec2 instance termination.
    - EBS Volumes are network drives with good but limited performance and can be retained once ec2 instance is terminated
    - EBS Volumes are of 6 types and which one to use depends on use case.
    - Consider these while selecting EBS [Volume type](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html) - size, throughput and IOPS (I/O operations per second)
    

    #### EBS Snapshots
    - Snapshots are backup of your EBS volumes at a point of time
    - Snapshots can be copied and moved to another AZ
    - Snapshots can be restored to create a copy of EBS Volume.
    #### [Know More about EBS Here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)

 - [Instance Store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html)

    - Instance store provides high performance(better I/O performance)
    - Instance store is lost once ec2 instance is terminated    
    - Instance Storage are good for cache/buffer/in-memory data, for long term store use EBS

- [EFS - Elastic File System](https://aws.amazon.com/efs/)

    

