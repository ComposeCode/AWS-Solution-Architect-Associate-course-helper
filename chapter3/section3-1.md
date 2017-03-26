# Chapter 1, Section 1: The S3 Storage Service

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

### Data Consistency Model for S3.

- Read after Write consistency for PUTS of new Objects
- Eventual consistency for overwrite PUTS and DELETES (can take some time to propagate).

What this means: When you PUT a new object into S3 you will get immediate consistency (you can read it instantly) however, when deleted or updating an object, you may have to wait some time to obtain the changes. When you read the data, you will either get the old data or the new data only (this is an atomic update). You will not get partial or corrupted data.

### S3 is a simple key, value store.

S3 is object based, objects consist of the following properties:

 - Key (This is simply the name of the object)
 - Value (This is the simply the data which make up the value)
 - Version ID (Important for versioning)
 - Metadata (Data about the data you are storing)
 
