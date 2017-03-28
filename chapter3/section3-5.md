# Chapter 3, Section 4: s3 Security & Encyrption

## Security

- By default all newly created buckets are Private.
- You can setup access control to your buckets using:
  - Bucket Policies
  - Access Control Lists
- S3 Buckets can be configured to create access logs which log all requests made to the S3 bucket. This cna be done ot another bucket.

## Encryption

- In transit Encryption: handled by SSL/TLS
- At REST:
      server side encryption: S3 Managed Keys - SSE-S3,  
      client-side encryption
