# AWS S3 Static Website Hosting Project

## Overview
In this project, I hosted a static portfolio website using Amazon S3's 
static website hosting feature, with public access configured through 
a bucket policy.

## Architecture
- S3 Bucket (public access enabled)
- Static Website Hosting (enabled via bucket properties)
- Bucket Policy (JSON-based public read access)
- HTML/CSS files (index.html, style.css)

## Steps Performed
1. Created an S3 bucket with a globally unique name
2. Disabled "Block all public access" to allow public website access
3. Uploaded index.html and style.css files to the bucket
4. Enabled Static Website Hosting in bucket Properties
5. Set index.html as the index document
6. Added a bucket policy to allow public read access (s3:GetObject)
7. Accessed the website via the S3 bucket website endpoint
8. Updated website content by re-uploading the modified index.html

## Bucket Policy Used
\`\`\`json
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
\`\`\`

## Skills Demonstrated
- S3 Bucket Management
- Static Website Hosting
- IAM/Bucket Policy Writing (JSON)
- Public Access Configuration
- Web Content Deployment & Updates

## Live Website
[View Live Website](http://my-portfolio-website-anees123.s3-website.eu-north-1.amazonaws.com/)
