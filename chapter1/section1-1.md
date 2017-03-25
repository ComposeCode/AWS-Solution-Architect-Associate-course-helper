# Chapter 1, Section 1: Overview

Before we begin, please make sure you have a valid AWS account with a valid credit card. This course was last updated in early 2017, changes to the course content may have already been made.

### What do you need to know?

You need to know a few core services, but knowledge of others is beneficial.

The core services required for the Certified Solutions Architect Associate exam are:

- Messaging
- Desktop & App Streaming
- Security and Identity
- Management Tools
- Storage
- Databases
- Compute
- Networking & Content Delivery
- AWS Global Infrastructure

These sections are broken down into specific services over the rest of the chapter.

### What are availability Zones?

AWS is made available globally across the world. Each location AWS is available is split into regions and availability zones. Each region is a separate geographic area. Each region has multiple, isolated locations, known as availability zones (they usually have 2 or more availability zones).

Simply put: an availability zone (AZ) is a data center. There are currently 14 regions with 38 availability zones.

Link: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html

### What are Edge Locations?

Edge Locations are CDN End Points for CloudFront, they act as cache. There are currently many more Edge Locations than regions, the current count being over 66.

Link: https://aws.amazon.com/about-aws/global-infrastructure/

### Networking & Content Delivery Services

## VPC: Virtual Private Cloud

A Virtual private cloud (VPC) is basically a virtual data center. It provides a virtual, dedicated network to your AWS account. It is logically isolated from other virtual networks in the AWS cloud.

In order to pass the exam you need to have a very good understanding of VPC and you should be able to build one from memory.

You can have multiple VPC per region and you can connect one VPC to another.

VPC Link: http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Introduction.html

## Route53: AWS DNS Service

This is Amazon's DNS service, named after the DNS Port (53) and the famous American Route 66 highway (https://en.wikipedia.org/wiki/U.S._Route_66).

Route 53 Link: https://aws.amazon.com/route53/

## Cloud Front: CDN/Cache service

CloudFront is part of the Content Delivery Network (CDN) and is part of the Edge Network. It can be used to cache assets, such as images and videos across these locations.

CloudFront Link: https://aws.amazon.com/cloudfront/

## Direct Connect: Dedicated Network Connection to AWS

Direct Connect provides a way to directly connect your physical datacenter to AWS using a dedicated network connection, instead of the internet. This provides a more reliable connection and improved security.

This can come up in the exam, but not very often.

Direct Connect Link: https://aws.amazon.com/directconnect/

### Compute Services

## EC2: Elastic Compute

EC2 stands for Elastic Compute and is the service which provides virtual machines, similar to on-prem VMware, OpenStack or just plain old KVM.

EC2 Link: https://aws.amazon.com/ec2/

## ECS: EC2 Container Service

EC2 Container Service is a highly scalable, high performing management service for running docker containers. It allows you to run applications on a cluster of EC2 instances (virtual machines). Removes the need for you to scale, managed, monitor your own Infrastructure (virtual machines).

This is not in the exam at all yet, may come up in the future.

## Elastic Beanstalk

Elastic Beanstalk service is an orchestration service is an orchestration service offered from Amazon Web Services for deploying infrastructure which orchestrates various AWS services including EC2, S3, Simple Notification Service (SNS), CloudWatch, AutoScaling and Elastic Load Balancers.

The idea of this service is to reduce the amount of knowledge required to use AWS. Using this service, you can upload your source code and Elastic Beanstalk will inspect your code and deploy the infrastructure required automatically.

Basic knowledge of the service is required (what it is) but more knowledge it is not required. It comes up infrequently in the solution architect exam, but comes up more frequently in the Developer exam.

Elastic Beanstalk Link: https://aws.amazon.com/elasticbeanstalk/

## Lambda

Lamdba is a serverless service provided by AWS. You do not manage any infrastructure, instead, you write code which is executed instead. This is significantly different to running Containers or Virtual Machines.

This will be covered but is not necessary to complete the exam.

Lambda Link: http://docs.aws.amazon.com/lambda/latest/dg/welcome.html

## Lightsail

Lightsail is a new service which has built-in deployment patterns. This is used to reduce the barrier to entry for cloud, extensive knowledge of AWS is not required to operate the service.

For example, if you wish to deploy something like a Wordpress blog, Lightsail is able to do that for you without needing to manage the infrastructure. This is similar to Canonical's Juju + Charms.

This is not in the SA exam.

Lightsail Link: https://amazonlightsail.com/

### Storage Services

## S3 Storage

The S3 Service provides object storage, it is perfect for storing individual files, such as pictures, documents or video. Used by companies like Dropbox. This service will be covered in the exam.

S3 Storage Link: https://aws.amazon.com/s3/

## Glacier

Glacier is used for long-term storage and is very low cost. It's very useful for backups of files and virtual machines which do not need to be accessed instantly. This service is useful if you need to store data for a long time which may be required for legal compliance.

This service comes up in the exam.

Glacier Link: https://aws.amazon.com/glacier/

## EFS (Elastic File System)

The EFS service provides block based storage which can be used by multiple virtual machines. This can be used to create virtual disks, which can be used by multiple virtual machines. This will come up in the exam so it is covered in detail.

EFS Link: https://aws.amazon.com/efs/

## Storage Gateway

The storage gateway service is used to connect on-premise datacenters to AWS and usually comes in the format of a virtual machine/virtual appliance. This is not in the exam.

Storage Gateway Link: https://aws.amazon.com/storagegateway/

### Databases

## RDS (Relational Database Service)

RDS provides relational databases as a service. This includes MySQL, Postgresql, MariaDB, Microsoft SQL Server, Oracle and Aura. This is covered in the course.

RDS Link: https://aws.amazon.com/rds/

## DynamoDB (NoSQL Database Service)

DynamoDB is a non-relational database service (similar to MongoDB). Very scalable and high performance. Covered but not in detail for the exam.

DynamoDB Link: https://aws.amazon.com/dynamodb/

## RedShift

RedShift is Amazon's data warehouse solution. This is used for running queries and other tasks on data outside of production databases. Not required for the Solution Architect course.

RedShift Link: https://aws.amazon.com/redshift/

## Elasticache

Elasticache is used to cache data in the cloud. If your application is designed correctly, you can design your application to store certain data in this service instead of your database to remove load off the database.

Elastiache Link: https://aws.amazon.com/elasticache/

### Migration Services

## Snowball

Snowball is used as a migration service for data. Amazon provide a device which they post to you (a big grey box full of disks) which you in turn fill up with data. Once the box is full, you post it back to Amazon and it gets stored in the cloud.

This service is included in the associate exam.

Snowball Link: https://aws.amazon.com/snowball/

## DMS (Database Migration Services)

Database migration service allows you to migrate on-prem databases to Amazon or existing databases on AWS to other regions or redshift and other cloud services.

At the same time, you can also convert your database to another type of database (for example, go from Oracle to AURA or another database type).

Not currently in the exam.

Database Migration Services: https://aws.amazon.com/dms/

## Server Migration Service (SMS)

This allows migration of virtual machines, up to 50 migrations concurrently. This is not in the exam.

Server Migration Service Link: https://aws.amazon.com/server-migration-service/

### Analytics Services

## Athena

This service allows you to run SQL queries on files. You can use flatfiles as regular databases. Not featured in the exams yet.

Athena Link: https://aws.amazon.com/athena/

## EMR (Elastic Map Reduce)

This service is used for Big Data. It is used to process large amounts of data (logs, financial data etc). This is part of Hadoop. A high level overview is required for the associate architects course.

EMR Link: https://aws.amazon.com/emr/

## Cloud Search / Elastic Search

Cloud Search is managed service provided by AWS for search functionality. Elastic Search is similar to Cloud Search but uses OpenSource products instead. Neither of these come up very often in the associate exams.

Cloud Search Link: https://aws.amazon.com/cloudsearch/
Elastic Search Link: https://aws.amazon.com/elasticsearch-service/

## Kinesis

Kinesis is used to perform analysis tasks on large amounts of data.  It is used a lot in the big data exam. You can use the service to capture many terabytes of data per hour.

Kinesis Link: https://aws.amazon.com/kinesis/streams/

## 
