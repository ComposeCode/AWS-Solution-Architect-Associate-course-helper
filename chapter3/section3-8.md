# Chapter 3, Section 8: S3 Transfer Acceleration

S3 Transfer Acceleration utilises the CloudFront Edge Network to accelerate your uploads to S3. Instead of uploading directly to your S3 bucket, you can use a distinct URL to upload directly to an edge location which will then transfer that file to S3. You will get a distinct URL to upload to:

    - URL Like: somename.s3-accelerate.amazonaws.com

## To enable S3 Transfer Acceleration

- Go to AWS -> S3 -> Go to the Bucket -> Click Transfer Acceleration -> From here, you can enable it.

- Note in gernal: the further you are away from an S3 region, the higher speed improvement you can expect from using the S3 Transfer Acceleration. 
