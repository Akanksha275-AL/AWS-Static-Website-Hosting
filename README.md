# AWS-Static-Website-Hosting
• Deployed an S3-hosted website with CloudFront for global content delivery. • Configured IAM policies for secure resource access.

Steps to Host on S3:
Create a Bucket

Go to S3 Console > Create bucket

Uncheck Block all public access

Name the bucket same as your domain (if using a custom domain)

Upload Files

Upload index.html, error.html, and any other assets (like images, CSS)

Set Permissions

Go to Permissions > Bucket Policy, paste:

json
Copy
Edit
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}

Enable Static Website Hosting

Go to Properties > Static Website Hosting

Choose “Enable”

Set index.html and error.html

Copy the endpoint URL (this is your website URL)


DONE


