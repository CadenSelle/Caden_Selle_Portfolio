# Portfolio Website - [cadenselle.com](https://cadenselle.com)

This is my personal portfolio website, built using HTML and CSS. Deployed using multiple AWS services
to gain real-world experience with cloud infrastructure and security best practices. 

The goal of this project was to learn how to deploy a fully static, secure, and globally distributed website using:
- Amazon S3 (static hosting)
- CloudFront (CDN)
- Route 53 (custom domain and DNS)
- Certificate Manager/ACM (SSL/TLS certificate)
- CloudWatch and CloudTrail (monitoring, alerting, and logging)

## Tools and Features:
  * **Frontend** - Built using HTML and CSS
  * **Static Hosting** - Hosted on Amazon S3
  * **Content Delivery** - Distributed via Amazon CloudFront for global low-latency performance
  * **Custom Domain** - Registered and routed through Route 53 (cadenselle.com and www.cadenselle.com)
  * **Budgets** - Created an AWS Budget with alerts sent via SNS when usage hits 80% or 100% of the monthly budget
  * **Monitoring and Alerts:**
      * **CloudWatch Syntehtics Canary** runs daily uptime checks and stores logs to a dedicated S3 bucket with a lifecycle policy to optimize storage and costs
      * **CloudWatch Alarm** is triggered if uptime check fails and sends a notification via SNS
  * **AWS CloudTrail** tracks and records all account-level API activity, with logs stored securely
  * **Security and IAM**:
      * **HTTPS Encryption** - Enabled using AWS Certificate Manager (ACM) with TLS for secure browsing
      * Created an **IAM User** with Administrator Access (MFA enabled) to manage AWS services securely instead of using the root account.
      * Configured **S3 Bucket Policies** to ensure only AWS services (Synthetics and CloudTrail) can write to dedicated logging S3 buckets

## Future Plans:
I plan to expand the website with blog posts, academic achievements, and technical documentation.  
Eventually, I will automate deployments using AWS CodePipeline or GitHub Actions for continuous delivery.
