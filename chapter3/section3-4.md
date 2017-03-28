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
