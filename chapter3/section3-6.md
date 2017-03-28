# Chapter 3, Section 6: Storage Gateway

- AWS Storage Gateway is a service that connects an on-premises software appliance with cloud-based storage to provide seamless and secure integration between an organization's on-premises IT environment and AWS's storage infrastructure. The service enables you to securely store data to the AWS cloud for scalable and cost-effective storage.

```
  need diagram of how this works.
```

- AWS Storage Gateway's software appliance is available for download as a virtual machine (VM) image that you install on a host in your datacenter. Storage gateway supports either VMware ESXi or Microsoft Hyper-V. Once you've installed your gateway and associated it with your AWS account through the activation process, you can use the AWS Management Console to create the storage gateway option that is right for you.

- Four types of storage gateway:
    - File Gateway (NFS)
    - Volumes Gateway (iSCSI)
      - Stored Volumes  
      - Cached Volumes
    - Tape Gateway (VTL)
