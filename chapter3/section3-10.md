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

- 
