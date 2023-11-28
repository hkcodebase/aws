# [CloudFront](https://aws.amazon.com/cloudfront/)

- Amazon CloudFront is a content delivery network (CDN) service built for high performance, security, and developer convenience.
- Improves read performance by caching content at 216 edge locations 
- Provides __DDoS__ Protection
- Integration with Shield, AWS Web Application Firewall 

## CloudFront Origins 
- S3 Bucket
  - For distributed files and caching them at the edge
  - Enhanced security with CloudFront Origin Access Control (OAC)
- Custom Origin(HTTP)
  - EC2 Instance
  - Aplication Load Balancer
  - S3 Website
  - Any HTTP backend you want

### [Example](https://aws.amazon.com/getting-started/hands-on/deliver-content-faster/) to Use CloudFront to serve content over S3 

## CloudFront Caching 
- Cache lives at CloudFront Edge Location
- Object is identified in cache using Cache Key
- Cache Hit Ratio maximize to minimize requests to origin
- Cache can be cleared/invalidated using CreateInvalidation API 