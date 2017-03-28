# Chapter 3, Section 4: Cloud Front Theory

### What is a CDN?

A content delivery network (CDN) is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage and a content delivery server.

```
  - Need in depth definition of CDN.
```

### CloudFront Terminology

- Edge Location: This is the location where content will be cached. This is separate to an AWS Region/Availability zone.

- Origin: This is the origin of all the files that the CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53.

- Distribution: This is name given to the CDN which consists of a collection of Edge Locations.

- Web Distribution: Typically used for Websites.

- RTMP - Used for Media Streaming

### What is CloudFront?

Amazon CloudFront is optimized to work with other Amazon web services, like Amazon Simple Storage Service (Amazon S3), Amazon Elastic Compute Cloud (Amazon EC2), Amazon Elastic Load Balancing and Amazon Route 53. Amazon CloudFront also works seamlessly with any non-AWS origin server, which stores the original, definitive versions of your files.

### CloudFront Exam Tips

- Edge Location: This is the location where content will be cached. This is separate to an AWS region/Availability zone.
- Origin: This is the origin of all the files that the CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53.
- Distribution: This is the name given to the CDN which consists of a collection of Edge Locations.
  - Web Distribution: Typically used for Websites.
  - RTMP - Used for Media Streaming.

- Edge locations are not just READ only, you can write to them too (put an object onto them).
- Objects are cached for the life of the TTL (time to live).
- You can clear cached objects, but you will be charged.

### Create a CloudFront Distribution

1) Log into AWS Console, go to S3. Go to a bucket with an image uploaded, or create a new one.

2) Once you have one setup, Go to Services -> (Under networking and Content Delivery) CloudFront and hit Create Distribution.
  - You can create either a web distribution or RTMP distribution.

3)  At the Create Distribution Screen:
  - Put in the origin domain name, in this case, it is the bucket name
  - A Distribution can have multiple origins (S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53).
  - The origin path can be a folder in the bucket itself.
  - The origin ID is a description for the origin. This value lets you distinguish multiple origins in the same distribution from one another. The description for each origin must be unique within the same distribution. The description for each origin must be unique within the distribution. (Important for Exam)
  - Restrict Bucket Access should be set to yes, this means all requests for your content must go through Cloud Front instead of directly to the bucket.
  - Create a New Identity (use the default value). This will create a new user to access your S3 data.
  - Grant Read Permissions on Bucket: Tick yes Update the Bucket Policy.

  - Path Pattern: You can setup regular expression for URL mapping.
  - Viewer Protocol Policy: Set which protocol (HTTP/HTTPS) can be used to view files. Set Redirect HTTP to HTTPS.
  - Allowed HTTP Methods: Set this to GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE (Allows you to set which HTTP Methods the Distribution can use)
  - Object Caching: Use Origin Cache Headers
  - Set the TTL values per object (time in seconds). The default TTL for all our objects will be cached at our edge locations for 1 day. 
