# Chapter 3, Section 7: Snowball

### What is snowball?

AWS Import/Export disk accelerates moving large amounts of data into and out of the AWS cloud using portable storage devices for transport. AWS Import/Export Disk Transfers your data directly onto and off of storage devices using Amazon's high-speed internal network and bypassing the Internet.

(Before Snowball, there are a system called Import-Export disk, where you can send your disks to Amazon).

Types of Snowballs: Snowball, Snowball Edge, Snowmobile.

```
  Need image of snowball device.
```

- Snowball is a petabyte scale data transport solution that uses secure appliances to transfer large amounts of data into and out of AWS. Using Snowball addresses common challenges with large-scale data transfers including high network costs, long transfer times, and security concerns. Transferring data with Snowball is simple, fast, secure and can be as little as one-fifth the cost of high-speed Internet.

80TB snowball in all regions. Snowball uses multiple layers of security designed to protect your data including tamper-resistant enclosures, 256-bit encryption, and an industry-standard Trusted Platform Module (TPM) designed to ensure both security and full chain-of-custody of your data. Once the data transfer job has been processed and verified, AWS performs a software erasure of the snowball appliance.

- The appliance is automatically erased after it has been delivered to remove the data.

- AWS Snowball Edge is a 100TB Data transfer device with on-board storage and compute capabilities. You can use Snowball Edge to move large amounts of data into and out of AWS, as a temporary storage tier for your large local datasets or to support local workloads in remote or offline locations.

Snowball Edge connects to your existing applications and infrastructure using standard storage interfaces, streamlining the data transfer process and minimizing setup and integration. Snowball Edge can cluster together to form a local storage tier and process your data on-premises, helping ensure your applications continue to run even when they are not able to access the cloud.

*Basically the same as regular snowball but with compute capability.

- Snowmobile:  AWS Snowmobile is an Exabyte-scale data transfer service used to move extremely large amounts of data to AWS. You can transfer up to 100PB per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck. Snowmobile makes it easy to move massive volumes of data to the cloud, including video libraries, image repositories, or even a complete data center migration. Transferring data with Snowmobile is secure, fast and cost effective.

## Exam Tips

- Understand what Snowball is
- Understand what Import Export is
- Snowball can:
  - Import to S3, Export from S3.
