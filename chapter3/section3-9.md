# Chapter 3, Section 9: S3 Static Website

## How to create a static website on S3 (lab)

- Log into AWS Console and go to S3
- Either go into an existing bucket or create a new one.
- Go to Properties of the Bucket -> Static Website Hosting.
- On this screen you will see the endpoint for the website provided by the bucket. You can also enable the static website here as well.
- Write an index.html file and upload it to the bucket.
- Go back to the Properties section and change the static website option index.html edit box to the value of your index.html file you just uploaded (it should be the filename).
- Follow the link and you should be able to view the home page.
