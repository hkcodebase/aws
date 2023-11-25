# [CloudFormation](https://aws.amazon.com/cloudformation/)

- AWS CloudFormation lets you model, provision, and manage AWS and third-party resources by treating infrastructure as code. 
- It is declarative way of outlining aws resources to be created, updated or destroyed

## Problem with Manual work
- Tough to reproduce exact resources in another region or another aws account
- Tough to reproduce exact resources in same region or aws account if resources are deleted

## Benefits
- Infrastructure as Code
  - Cloud Formation creates resources in the right order with exact configuration
  - Resource don't need to be created manually so easy to control
  - Code can be version controlled using git
- Cost
  - Each resources within stack is tagged with an identifier so you can track the cost of an stack
  - Cost can be estimated using CloudFormation Template
  - Save cost : Automatic delete all resources when not needed and create them when required
- Productivity
  - Ability to destroy and re-create an infrastructure in the cloud on the fly
  - Automate generation of diagram for your templates
  - Declarative programming
- Separation of Concern: Create many stack for many apps, and many layers. Ex - 
  - VPC Stack
  - Network Stack
  - App Stack
- Don't reinvent the wheel

## How CloudFormation Works
- Templates have to be uploaded in S3 and then referenced in CloudFormation
- To update a template create a new version, we can't edit previous one.
- Stacks are identified by name
- Delete a stack deletes all artifacts created by cloudformation using that stack

## Deploying CloudFormation Templates
- Manual Way
  - Editing templates in CloudFormation Designer
  - Using the console to input parameters, etc
- Automatic Way (__Recommended way__)
  - Editing templates in a YAML File
  - Using the AWS CLI(Command Line Interface) to deploy templates

## CloudFormation Template
- Can be prepated using JSON or YAML
- Needs these values -
  - Resources (Mandatory)
    - Different AWS Components that will be created
    - Resources are declared and can reference each other
    - There are 224 [resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html) types in AWS 

