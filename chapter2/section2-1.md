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

14) Create an IAM Password Policy (IAM -> Account Settings). No reuse, etc.

15) Create a new Role (IAM -> Go to Roles), select a policy, put in a name, hit create.

### Creating Billing Alarms

A billing alarm will send you a notification if you spend a certain amount of funds on Amazon.

1) Log into AWS Console.

2) Click your name (top right) and hit My Billing Dashboard.
  - https://console.aws.amazon.com/billing/home#/

3) At the bottom, it says Alerts and Notifications.

  - Click 'Enable Now' for: Monitor your estimated charges. Enable Now to begin setting billing alerts that automatically e-mail you when charges reach a threshold you define.

4) On the next page, hit Receive Billing Alerts and then hit save preferences. Note that this feature cannot be disabled once it has been enabled.

5) Go back to the console -> Services -> Management Tools -> Cloud watch

6) Go to Alarms -> Billing and hit create alarms.

7) Create a billing alarm and verify the email address. If the estimated charge exceeds the limit you set, you should receive an email.

Summary: This can come up in the exam, important to know how to configure it.

### IAM Summary

IAM consists of:
 - Users
 - Groups (A way to group users and apply policies to them collectively),
 - Roles
 - Policy Documents.

Example Policy Document:

```
  {
      "Version": "2012-10-17",
      "Statement":
        [
          {
              "Effect": "Allow",
              "Action": "*",
              "Resource": "*",
          }
        ]
  }
```

- IAM is Universal, it does not matter which region you are in.

- The root account is the account created when you first create your AWS account. This has the highest level of privileges and should be locked down and rarely used.

- New users has no permissions when they are first created. They must be assigned privileges.

- New Users are assigned Access Key ID and Secret Access Keys when first created. These are not the sae as a password, and you cannot use the access key ID & secret access to log into the console. You can use this to access AWS via the APIs and Command Line however.

- You only get to view those credentials once, they should be saved otherwise you will have to regenerate them.

- You should enable multifactor authentication (MGA) on your root account.

- You can create and customise your own password rotation polices.
