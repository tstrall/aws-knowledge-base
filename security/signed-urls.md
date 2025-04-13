# Signed URLs & Signed Cookies

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Signed URLs and signed cookies** are mechanisms used to grant **temporary, restricted access** to private content hosted in Amazon **CloudFront** or **S3**. They let you serve content securely without making it publicly available.

- **Signed URL** – Grants access to a specific file.
- **Signed cookie** – Grants access to multiple files (e.g., all in a path) based on user session.

---

## Why should I care?

These tools are critical for protecting **private media, documents, or downloads**:

- Control who can access your content and for how long.
- Enforce expiration times, IP address restrictions, and path constraints.
- Avoid exposing S3 buckets or CloudFront distributions to the public.

They’re frequently used in **media streaming**, **paywall systems**, and **download portals**.

---

## When to use it

Use signed URLs or cookies when:

- You need to **restrict content access** based on user or session context.
- You want to serve private content via **CloudFront CDN** or **S3 directly**.
- Your app generates **temporary links** (e.g., for file download or video playback).
- You want to restrict access by **IP, time, or path**.

---

## Key features

- **Time-limited access** – Set expiration on links or cookies.
- **IP address restrictions** – Only allow specific IPs or IP ranges.
- **Path filtering** – Limit access to a specific directory or object prefix.
- **Private key signing** – You create signed tokens using a trusted private key.
- **CloudFront key groups and trusted key IDs** – Enable central control for multiple URLs.

---

## Common use cases

- **Streaming video or audio** – Provide limited-time playback for authenticated users.
- **Secure file downloads** – Share content without exposing your S3 bucket.
- **User-specific content** – Ensure users only access the data they're authorized to see.
- **Paywalled content** – Grant access after a payment or authentication event.

---

## Integrations

- **Amazon CloudFront** – Commonly used with signed URLs and cookies for content delivery.
- **Amazon S3** – Works with pre-signed URLs for object-level access.
- **Lambda@Edge** – Can generate signed URLs at the CDN edge.
- **Cognito / IAM** – Used to authenticate users before generating signed access tokens.

---

## Example: Pre-signed S3 URL

```python
import boto3
s3 = boto3.client('s3')
url = s3.generate_presigned_url(
    ClientMethod='get_object',
    Params={'Bucket': 'my-private-bucket', 'Key': 'file.pdf'},
    ExpiresIn=3600  # 1 hour
)
```

---

## Pricing

There is **no extra charge** for using signed URLs or cookies.  
You pay only for the underlying **S3** and **CloudFront** usage (requests, data transfer, etc.).

---

## Learn More

- [Serving Private Content with CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html)
- [S3 Pre-signed URLs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ShareObjectPreSignedURL.html)
- [Lambda@Edge for Auth & Signing](https://docs.aws.amazon.com/lambda/latest/dg/lambda-edge.html)
- [CloudFront Signed URLs vs Signed Cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html)
