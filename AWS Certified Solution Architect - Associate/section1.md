# AWS Solutions Architect - Associate

## Exam

* 130 min
* 60 questions
* Multiple Choice
* Results 100 - 1000
* Pass mark of 70%
* Qualification valid for 2 years
* Scenario based questions

## IAM

* Manage users and their level of access to the AWS console.
* Centralised Control of the your AWS account
* Shared access 
* Granular Permissions
* Identify Federation
* Multi-factor Authentication
* Provide temporary access.
* Password rotation
* Integrates with many different AWS services.
* PCI DSS


> IAM is global.
> "root account" is simply the account created when first setup your the AWS account. It has complete admin access
> New users have NO permissions when first created
> New Users are assigned Access Key and Secret Access keys when first created
> These are just api credentials.


### Users

End users ad people

### Groups

collection of users

### Policies

made of documents (JSON)

### Roles

Create roles then assign them to AWS resources.

# S3

Simple Storage Service

* S3 is a safe place to store your files
* Object based
* Unlimited Storage
* Buckets = Folder
* S3 universal namespace - unique globally
* key / value / versionId / metadata / sub resource 

> Read after write consistency PUTS for new object
> Eventual consistency for overwrite PUTS and DELETES (Can take time to propergate)
> Built for 99.99% availability for S3 platform
> Amazon guarantee 99.9% availability 
> Amazon guarantee 11x9s durability

* Tiered storage available
* Lifecycle Management
* Versioning
* Encryption
* MFA Delete
* Secure data using ACL and bucket policies

## S3 Storage Classes

S3 Standard

* 4 x9s availability
* 11 x 9s durability
* Redundant across multiple facilities
* Designed to sustain loss of 2 facilities concurrently

S3 - IA (Infrequently Accessed)

* For data that is access less frequently
* But requires rapid access
* Lower fee than S3
* Charges a retrieval fee

S3 One Zona - IA

Lower cost options for infrequently access data but do not require multiple availability zone data resilience.

S3 - Intelligent Tiering

Designed to optimise costs by automatically moving data to the most cost effective access tier without performance impact or operational overhead.

S3 Glacier

* Data archiving
* retrieval times minutes -> hours

S3 Glacier Deep Archive

* lowest cost and retrieval time in hours 
* ie 12 hours

S3 charge

* Storage
* Request 
* Storage Management Pricing
* Data Transfer Pricing
* Transfer Acceleration
* Cross region replication pricing

> ! Read through S3 (FAQ)[!https://aws.amazon.com/s3/faqs/]

## S3 Security

Encryption at rest

* S3 managed keys - SSE-S3
* AWS Key Management Service - Managed Keys - SSE-KMS
* Server Side Encryption with Customer provided Keys - SSE-C
* Client Side Encryption

Using versioning with S3

* Stores all versions of the object
* Great backup tool
* Once enabled cannot be disabled - Only suspended
* Integrates with Lifecycle rules
* Versioning's MFA Delete capability - which uses multi factor authentication.


