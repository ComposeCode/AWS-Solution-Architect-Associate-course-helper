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
