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

### What are availability Zones?

AWS is made available globally across the world. Each location AWS is available is split into regions and availability zones. Each region is a separate geographic area. Each region has multiple, isolated locations, known as availability zones (they usually have 2 or more availability zones).

Simply put: an availability zone (AZ) is a data center. There are currently 14 regions with 38 availability zones.

Link: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html

### What are Edge Locations?

Edge Locations are CDN End Points for CloudFront, they act as cache. There are currently many more Edge Locations than regions, the current count being over 66.

Link: https://aws.amazon.com/about-aws/global-infrastructure/

### Networking & Content Delivery Services

## VPC: Virtual Private Cloud

A Virtual privae cloud (VPC) is basically a virtual datacenter. It provides a virtual, dedicated network to your AWS account. It is logically isolated from other virtual networks in the AWS cloud.

In order to pass the exam you need to have a very good understanding of VPC and you should be able to build one from memory.

You can have multiple VPC per region and you can connect one VPC to another.

VPC Link: http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Introduction.html

## Route53: AWS DNS Service

This is Amazon's DNS service, named after the DNS Port (53) and the famous American Route 66 highway (https://en.wikipedia.org/wiki/U.S._Route_66).

Route 53 Link: https://aws.amazon.com/route53/

## Cloud Front: CDN/Cache service
