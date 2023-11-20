# [AWS CLI](https://aws.amazon.com/cli/) - Command Line Interface

- Command Line Interface to connect to AWS Services
- Credentials Provider Chain -
    - Command Line Options - --region --output and --profile
    - Environment Variables - AWS_ACCESS_KEYS_ID, AWS_SECRET_ACCESS_KEY, AWS_SESSION_TOKEN
    - CLI Credentials File - ``` command - aws configure, File(Mac) - ~/.aws/credentials``` 
    - CLI Configuration File - ``` command - aws configure, File(Mac) - ~/.aws/config```
    - Container Credentials - for ECS Tasks
    - Instance Profile credentials - for EC2 Instance Profiles



# AWS SDK 
- Java SDK Credentials lookup Chain -
    - System Properties - aws.accessKeyId, aws.secretKey
    - Environment Variables - AWS_ACCESS_KEYS_ID, AWS_SECRET_ACCESS_KEY
    - Default Credentials File - ``` ~/.aws/credentials``` 
    - Amazon ECS Container Credentials - for ECS Containers
    - Instance Profile credentials - used on EC2 Instance

# Credentials Best Practice

 - *Never Store Credentials in your code*
 - Credentials should be inherited from credentials chain
 - Within AWS, use IAM Roles 
    - EC2 Instance role for EC2 instances
    - ECS Roles for ECS tasks
    - Lambda Roles for Lambda functions
- Outside AWS : use environment variables/ named profiles