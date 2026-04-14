**S3 Static Website with CloudFront CDN**
<br>
<br>
**Overview**

This project demonstrates hosting a static website using Amazon S3 and delivering it globally using Amazon CloudFront.

**Architecture**

User → CloudFront → S3 Static Website

**Services Used**
Amazon S3 (object storage and static website hosting)
Amazon CloudFront (content delivery network)
Implementation Steps
<br>
<br>
**1. Create S3 Bucket**
<br>
<br>
Created a globally unique bucket name
Selected correct AWS region
<br>
<br>
**2. Enable Static Website Hosting**
<br>
<br>
Enabled static website hosting in bucket properties
<br>
<br>
Defined: index.html as default document
<br>
<br>
**3. Upload Website Files**
<br>
<br>
Created index.html locally
Uploaded file to S3 bucket
<br>
<br>
**4. Configure Bucket Policy**
Added policy to allow public read access
<br>
<br>
**5. Verify S3 Website Endpoint**
Accessed S3 website URL
Confirmed site loads successfully
<br>
<br>
**6. Create CloudFront Distribution**
Created distribution using S3 website endpoint
Configured origin to use: s3-website endpoint (not standard S3 endpoint)
<br>
<br>
**7. Configure Origin Settings**
Set origin protocol policy to HTTP only
Ensured compatibility with S3 static hosting
<br>
<br>
**8. Disable Security Protections (WAF)**
Chose not to enable AWS WAF to avoid additional costs
<br>
<br>
**9. Deploy and Test CDN**
Waited for CloudFront deployment
Accessed CloudFront URL
Verified website loads globally
Key Learnings
Difference between S3 bucket endpoint and website endpoint
How CloudFront integrates with S3
How CDN improves performance and availability
Troubleshooting Access Denied errors
Importance of correct origin configuration
Challenges Faced
CloudFront configuration differences in AWS console
Access Denied errors due to incorrect origin setup
Understanding S3 permissions and bucket policies
<br>
<br>
**Outcome**

Successfully deployed a fully serverless static website using S3 and CloudFront with global content delivery.
