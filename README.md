# AWS S3 Static Website

 Project Overview

This project demonstrates how to deploy and host a static website
using Amazon S3.

The project was built as part of my AWS Cloud Engineering
hands-on portfolio after completing the AWS Cloud Practitioner
(CL​​F-C02) certification.

 Architecture

User
  │
  ▼
Amazon S3
  │
  ├── index.html
  ├── style.css
  └── error.html
  │
  ▼
Static Website

 AWS Services Used

- Amazon S3
- AWS IAM
- Amazon CloudWatch

 Technologies

- HTML5
- CSS3
- Git
- GitHub
- AWS

 Implementation Steps

1. Created an S3 bucket.
2. Uploaded the website files.
3. Enabled S3 Static Website Hosting.
4. Configured the index document.
5. Configured a custom error document.
6. Disabled Block Public Access for this learning project.
7. Created an S3 bucket policy allowing public `GetObject`.
8. Tested the website through the S3 website endpoint.
9. Version-controlled the project using Git.
10. Pushed the project to GitHub.

 Bucket Policy

The bucket uses the following policy to allow public
read access to website objects:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}