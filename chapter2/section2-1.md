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

### Using IAM

```
  need screenshots of using IAM
```

1) Log into AWS console

2) Go to IAM in the console

3) Note that IAM is applied globally (note, this changes in the top right hand side)

4) Change the single users sign in link (This creates an ALIAS domain for logging into IAM)

5) The root account is the initial account created as part of the sign up and most likely contains the credit card details and highest privileges etc.

6) Enable Multifactor Authentication (MFA) on your root account - need example using mobile phone or another device.

7) Create a new user (put in some users, set a password policy). When going to set permissions, hit 'add users to group'

8) Create a new group (create a new group called system administrators). Each policy is a document (you can see the document if you click on a policy).
9) Create Users

10) Explain the access key ID, secret access key and the password for the new accounts.
   - The secret access key ID is used for API calls.
   - You can also send an email to your users containing Login instructions.

11) Create a new group which has read only access to S3 buckets. Assign one of the users to the S3 bucket.

12) Go to IAM -> Users -> Click a newly created user. Under Permissions you can see the available policies he has.

13) Security Credentials: this tab of a user can be used to create new access keys, make access keys inactive and create SSH keys for code commit.

14) Create an IAM Password Policy: 
