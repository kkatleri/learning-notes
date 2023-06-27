# AWS Solution Architect - Associate (SAA-C03)

- [Introduction](#Introduction)
- [AWS Fundamentals](#aws-fundamentals)
- [Identity Access & Management (IAM)](#identity-access--management)


## Introduction
Exam Pattern

- Design Resilient Arch - 26%
- Design High Performing Arch - 24%
- Design Secure Arch - 30%  *****IMP******
- Design Cost-Optimized Arch - 20%

Passing Mark - 725/1000
65 Questions/ 135 Minutes

## AWS Fundamentals

- Building blocks of AWS
    - Region - Its a geographical/physical location consists of 2 or more Availability Zones
    - Availability Zone - It is a one or more discrete data centers in a particular region 
    - Edge location - It is an AWS endpoints for caching and serving static content
    - More edge locations than regions

- Shared responsibility model
    - AWS/ You/ Shared(Encryption)
    - can you do it yourself through AWS Mgmt console ??

- AWS Key services
    - Compute - EC2, Lambda, Elastic Beanstalk
    - Storage - S3, EBS, EFS, FSx, Storage gateway
    - Database - DynamoDB, RDS, Redshift
    - Networking - VPN, Direct Connet, API Gateway, Route 53, AWS Global Accelerator 

- Well-Architected Framework
    - 6 pillers of well-archietect framework
    - Opertional Excellence
    - Performance Efficiency
    - Cost optimization
    - Security
    - Reliability
    - Sustainability

## Identity Access & Management
- AWS Root account must be secured with 2-factor authentication
- Should create admin group with appropriate permissions and add user to it for Admin access
- IAM is a global service, its not specific to any region
- User, roles & groups are created at global level & available in all the regions
- User is created for each physical person (One user for one person)
- When user is created it provides Access key and scecet key for programmatic access
- Role is internal for AWS services (non-person entity)
- Permission is set of rules defined using IAM Policy Document that can be assinged to either user, role or group to define level of access.
- Example IAM Policy Document
```
{
    "version":"",
    "Statement":[
        {
            "Effect":"Allow",
            "Action":"*",
            "Resource":"*"
        }
    ]
}
```
- Ability for IAM Federation & Identity Federation
    


