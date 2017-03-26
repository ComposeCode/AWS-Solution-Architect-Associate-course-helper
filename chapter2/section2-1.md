# Chapter 1, Section 1: Identity Access Managaement (IAM)

This service allows you to configure who is able to access your account on the AWS console. You can create user groups, modify user permissions and perform other actions in this section of the AWS Console. This is part of the exam and we will now cover it in detail.

```
  Need screenshots of logging into console and going to IAM.
```

What does IAM Provide?

- IAM Provides a Centralised Control of your AWS Account (from within IAM, you can change user settings, permissions, etc)
- You can use IAM to configure shared access to your account.
- You can peer accounts to other accounts
- You can set user permissions so they can only use certain AWS services
- Identity Federation (including Active Directory, Facebook, LinkedIn, etc)
- Multifactor Authentication (two factor, etc)
- Provide Temporary acess for users/devices and services where necessary
- Allows you to set password policy (rotation, strength, etc)
- Integrates with many AWS services.
- Supports PCI DSS Compliance.

Critical Terminology:

- Users: These are end users (people)
- Groups: These are a collection of users under one set of permissions.
- Roles: You Create Roles and can then assign them to AWS resources
- Policies: A document that defines one (or more permissions)

###
