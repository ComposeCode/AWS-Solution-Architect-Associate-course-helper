# Chapter 3, Section 10: S3 Summary

## Exam Tips

- Remember that S3 is Object based i.e. allows you to upload 'flat files', not used as a blockstore for OS or databases, etc (EBS shoudld be used for that)
- Files can be from 0 bytes to 5TB.
- There is unlimited storage
- Files are stored in buckets.
- S3 is a universal namespace, that is, names must be unique globally.
- http://s3-euwest-1.amazonaws.com/somebucketname
- New Objects: Read after Write consistency for PUTS of new Objects.
- Update or Delete an Object: Eventual Consistency for overwrite PUTS and DELETS (can take some time to propagate, may access an older version)

- S3 Storage Classes/Tiers:
    - S3 (Durable, immediately available, frequently accessed)
    - S3 - IA (durable, immediately available, infrequently accessed)
    - S3 Reduced Redundancy Storage (data that is easily reproducible, such as thumb nails etc)
    - Glacier - Archived Data, where you can wait 3-5 hours before accessing.

- Remember the core fundamentals of S3:
  - Key (Name)
  - Value (data)
  - Version ID
  - Metadata
  - Access Control Lists

- Object based storage only (for files), not suitable for an OS or database.

- S3 - Versioning: Store all versions on an object (including all writes and even if you delete an object). Good for keeping backups.

- Integrates with Lifecycle Rules

- Versioning's MFA Delete capability, which uses multi-factor authentication, can be used to provide an additional layer of security.

- Cross Region replication, requires versioning enabled on the source bucket/destination bucket.

- Edge Location: This is the location where content will be cached. This is separate to an AWS region/Availability zone.

- Origin: This is the origin of all the files that the CDN will distribute. This can either be an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53.

- Distribution: This is the name given to the CDN which consists of a collection of Edge Locations (two types of distribution):
  - Web Distribution: Typically used for Websites.
  - RTMP: Used for Streaming video/flash files.

- Edge Locations are not just READ ONLY, you can write to them too (I.E put objects on them)
  - Objects are cached for the life of the TTL (Time To Live).
  - You can clear cached objects, but you will be charged.

- All newly created buckets are PRIVATE

- You can setup access control to your buckets using:
  - Bucket Policies
  - Access Control Lists

- S3 Buckets can be configured to create access logs which log all requests made to the S3 bucket. This can be done to another bucket.

- Encryption:
  - In Transit: using SSL/TLS,  
  - Server Side: S3 Managed Keys (SSE-S3, uses AES-256), AWS Key Management Service (Managed Keys, SSE-KMS, Envelope Key), Server side Encryption with Customer Provided Keys (SSE-C)
  - Client Side

### Lifecycle Management

- Lifecycle Management: can be used in conjunction with versioning.

- Can be applied to current versions and previous versions.

- Following actions can now be done:

  - Transition to the Standard - Infrequent Access Storage Class (128KB in size + 30 days after the creation date).
  - Archive to the Glacier Storage Class (30 days after IA, if relevant).
  - Permanently delete objects with lifecycle rules.
