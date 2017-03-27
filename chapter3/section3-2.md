# Chapter 3, Section 1: Using S3 from the AWS Console

### Using S3

First log into the AWS Console, then perform the following steps:
- Click into services, click into S3.
- Create a new Bucket (name must be unique), select any region.
- Click on the newly created bucket and hit properties. The properties allow you to check/enable logging, versioning, events, tags etc. You can also host a static website out of S3.
- The Permissions tab: In here we have access control lists, by default the buckets are set to private.
- Management Tab -> Lifecycle: This contains lifecycle management, we can tier data to different S3 Tiers (I.E data is 30 days old, move to infrequently accessed storage etc).
- Management Tab -> Analytics: This gives us the ability to perform analytics on the data in the bucket (may show ways to save money)
- Management Tab -> Metrics: This shows metrics for data in our bucket (total storage, transfer rates etc)
- Management Tab -> Inventory: These are reports on what is actually in our buckets.

## Upload a file to S3

- Click on the bucket and hit the objects tab.
- Hit the Upload Button, and then hit add files.
- Upload a random file (select a picture or something else)
- Hit next to set permissions, leave it as default.
- On the next page we can set properties: Which storage class (types of S3 discussed previously), do we want encryption on the file, do we want to attach metadata to the file?
- Go through and hit next until the upload button is hit and the file is available in the bucket (should be in the object list).

- Note that if you click the file, you can see the Link to the file. Note if you click the file, you will get an accessed denied error. This is because the default permissions are set to deny.

- To change this, click the file and go to permissions, you can then set user based permissions or permissions for anyone (read/write, etc.). If you set the Everyone permission to read/read, anyone can now see this/download this file.

- If you click on the file and then hit the properties tab, you can change the storage class of the file (infrequently accessed or reduced redundancy etc). You can also add server side encryption to the image/file you used.

## Enable Versioning

To enable versioning, it can be done on the properties tab for a bucket. You can modify versioning on existing or new buckets.

When setting permissions, you have Object Access and Permissions Access. Object access grants a user permissions to list, create, overwrite or delete objects in the bucket. Permissions access allows you to grant a user read or write access to an access control list (ACL) for the bucket.

Before we begin, change the Permissions on the bucket so that Everyone has read object access.

Once versioning has been enabled, it cannot be removed, only disabled. This is a key point for the exam.

1) Outside of the console on your computer, create a text file with some text called test.txt

2) Upload the file to AWS, make sure versioning is enabled on the bucket before hand. When you Upload the file make sure the read permission for everyone is to read.

3) When you click on the file in the bucket, you should have the option to check the Latest Version of the file. Make the file public and check its contents in the browser.

4) Try re-uploading the file, you should notice that another version becomes available. You can download newer and older version of the file.
  - Notice that when you change the file the etag of the file changes.
  - The total bucket size is the size of each version for each file (so multiple changes to a file add up disk space).
  - From architectural point of view, versioning requires some constraint, you will need to cull old versions at some point and archive them to Glacier at some point.
  - Though it looks like one file, it is actually storing multiple files. The total size is the sum of size of all versions of the file.

## Restoring a deleted file

1) Go back to the bucket and click the tick next to the file to be deleted. Go to more -> Delete and delete the file.

2) 
