# Chapter 3, Section 3: Lifecycle Management and Glacier

## Lifecycle Management Lab

Lifecycles, when applied to storage, are used to help you reduce your storage costs by controlling the lifecycle of your objects. These can be used to automatically migrate and move your storage to cheaper tiers to save money.

1) Log into AWS Console, go to Storage, go to S3.

2) Delete the previous bucket: Click the bucket and then hit 'Delete Bucket' button when it turns blue.

3) Go to an existing bucket or create a new bucket.

4) Go to Management -> Lifecycle

- Glacier is still not available in some regions.

5) Enter a name for the transition, such as 'mylifecyclerule', press next.

6) On the next page, select both current and previous versions under configure transition.

7) If you see a message which says 'You don't have any transitions set up for your current version of objects', hit Add Transition.
  - Hit add transition. From the drop down, select 'Transition to Standard-IA after' and in the 'Days After Object Creation' box, put in an integer, such as 30.
  - Hit add transition. From the drop down, select 'Transition to Amazon Glacier after' and in the 'Days After Object Creation' box, put in an integer, such as 30.
