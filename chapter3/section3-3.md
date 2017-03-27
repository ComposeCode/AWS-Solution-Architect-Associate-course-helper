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
  - Hit add transition. From the drop down, select 'Transition to Amazon Glacier after' and in the 'Days After Object Creation' box, put in an integer, such as 60.
  - Repeat the above for the 'Previous Versions' transitions, if the 'Previous Versions' is also selected.

8) Hit the next button and go to the Expiration page:
  - Select configuration expiration for Current and Previous Versions.
  - Expire current version of object: this should be set to a value greater than the previous value set (I.E 61).
      - Note that for versioned systems, the current version is marked as a previous version and a delete marker will be set at the current version if the expiration period is met.
      - This is similar to a 'soft-delete option'
  - The permanently delete previous versions should also be configured. This will permanently remove files after a certain period.
      - This is a permanent delete option.

 ## Exam Tips

 - Lifecycle management can be used in conjunction with versioning.
 - Lifecycles can be applied to current versions and previous versions.
 - Following actions can now be done:
    - Transition to the standard, infrequent access storage class (128kb and 30 days after the creation date).
    - Archive to the Glacier Storage Class (30 days after IA, if relevant).
    - Permanently delete files after a certain amount of time.
