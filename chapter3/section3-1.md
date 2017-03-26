# Chapter 3, Section 1: The S3 Storage Service

### What is S3 Storage?

Definition: S3 stands for simple storage service and it provides developers and IT Teams with secure, durable, highly-scalable object storage. Amazon S3 is easy to use, with a simple web services interface to store and retrieve any amount of data from anywhere on the web.

S3 is a place to store your files (pictures, movies, music, etc) in the cloud. It is an object based storage service (not block store). The data is spread across multiple devices and facilities.

### The basics

- S3 is Object Based i.e. allows you to upload files. F
- Files can be from 0 bytes to 5TB.  
- There is unlimited storage.
- Files are stored in buckets.
- S3 is a universal namespace, that is, names must be unique globally.
- When files are uploaded to S3, you will receive a HTTP 200 code once the file has been uploaded successfully (http codes are important for the exam).
- Built for 99.99% availability (Amazon Guarantee)
- Built for 99.99% durability for S3 Information 99.999999999% (remember 11 x 9's)
- Tiered Storage Options
- Lifecycle Management
- Versioning of Files
- Encryption of Files
- Secure data using Access Control Lists (ACL) and Bucket Policies

### Data Consistency Model for S3.

- Read after Write consistency for PUTS of new Objects
- Eventual consistency for overwrite PUTS and DELETES (can take some time to propagate).

What this means: When you PUT a new object into S3 you will get immediate consistency (you can read it instantly) however, when deleted or updating an object, you may have to wait some time to obtain the changes. When you read the data, you will either get the old data or the new data only (this is an atomic update). You will not get partial or corrupted data.

### S3 is a simple key, value store.

S3 is object based, objects consist of the following properties (each file you upload will have these properties)

 - Key (This is simply the name of the object)
 - Value (This is the simply the data which make up the value)
 - Version ID (Important for versioning)
 - Metadata (Data about the data you are storing)
 - Sub resources (Made up of Access Control Lists, Torrent)

### Different Storage Tiers/Classes

S3 is designed to be redundant in the event of the loss of facilities. Files are stored across multiple devices in multiple facilities. Very highly available.

S3 - IA (Infrequently Accessed) for data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee.

Reduced Redundancy Storage: Designed to provide 99.99% durability and 99.99% availability of objects over a given year.

Glacier: Very cheap, but used for archival only. It takes 3-5 hours to restore from Glacier.

Which option do I pick? It comes down to retrieval time and cost considerations. Questions in the exam will focus around which option to pick based on a given scenario.  

```
  Need table comparing different Tiers/Classes of S3 storage.
```

Note all services support SSL.

## What is Glacier?

Glacier is a separate service to S3: It is an extremely low-cost storage service for data archival. Amazon Glacier stores data for as little as $0.01 per gigabyte per month, and is optimized for data that is infrequently accessed and for which retrieval times of 3 to 5 hours are suitable.
