# Chapter 4, Section 1: EC2 Introduction

### What is EC2?

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud. Amazon Ec2 reduces the time required to obtain and boo new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirements change.

Amazon EC2 changes the economics of computing by allowing you to pay only for capacity that you actually use. Amazon EC2 provides developers the tools to build failure resilient applications and isolate themselves from common failure scenarios.

- Virtual Machines, on demand.

## EC2 - Options

- on Demand - allow you to pay a fixed rate by the hour with no commitment.
- Reserved - provide you with a capacity reservation, and offer a significant discount on the hourly charge for an instance. 1 Year or 3 Year Terms.
- Spot, enable you to bid whatever price you want for instance capacity, providing for even greater savings if your applications have flexible start and end times.
- Dedicated Hosts - Physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allow you to use your existing server-bound software licenses.

## On Demand

- Users that want the low cost and flexibility of Amazon EC2 without any up-front payment or long-term commitment.
- Applications with short term, spiky or unpredictable workloads that cannot be interrupted.
- Applications being developed or tested on Amazon EC2 for the first time.

## Reserved

- Applications with steady state or predictable usage.
- Applications that required reserved capacity.
- Users able to make upfront payments to reduce their total computing costs even further (locked in 1-3 year contract, locked in, can pay up-front).
- Applications with steady state or predictable usage.

## Spot

- Spot prices change on region/availability zone
- Set a bid price for your compute. When the spot price and bid price are the same, compute power will be purchased.
- If your spot price moves about your bid price, then your instances are terminated.
- Applications that are only feasible at very low compute prices.
- Applications that have flexible start and end times.
- Users with urgent computing needs for large amounts of additional capacity.

## Spot Exam Tip
- If the spot instance is terminated by Amazon EC2, you will not be charged for a partial hour of usage. However, if you terminate the instance yourself you will be charged for any hour in which the instance ran.

# Dedicated Hosts

- Useful for regulatory requirements that may not support multi-tenant virtualisation.
- Great for licensing which does not support multi-tenancy or cloud deployments.
- Can be purchased On-Demand (hourly)
- Can be purchased as a reservation for up to 70% off the On-Demand Price.

# EC2 Instance Types

```
  Need Family Types Table for Instance Types
```

Anagram: DIRTMCGFPX

Doctor Mc GIFT PX

D is for Density
R is for Ram
M is for main choice general purpose apps
C is for Compute
G is for Graphics
I is for IOPS
F is for FPGA
T cheap general purpose (think T2 Micro)
P - Graphics think pictures
X - Extreme Memory

## What is EBS?

Amazon EBS (Elastic Block Storage) allows you to create storage volumes and attach them to Amazon EC2 instances. Once attached, you can create a file system on top of these volumes, run a database, or use them in any other way you would use a block device. Amazon EBS volumes are placed in a specific Availability Zone, where they are automatically replicated to protect you from the failure of a single component.

EBS Volume Types:

- General Purpose SSD (GP2)
  - General purpose, balances both price and performance.
  - Ratio of 3 IOPS per GB with up to 10,000 IOPS and the ability to burst up to 3000 IOPS for extended periods of time for volumes under 1GiB.

- Provisioned IOPS SSD (IO1)
  - Designed for I/O intensive applications such as large relational or NoSQL databases.
  - Use if you need more than 10,000 IOPS
  - Can provision up to 20,000 IOPS per volume.

- Throughput Optimized HDD (ST1)
  - Big Data
  - Data Warehouses
  - Log Processing
  - Cannot be a boot volume
