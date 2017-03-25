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
