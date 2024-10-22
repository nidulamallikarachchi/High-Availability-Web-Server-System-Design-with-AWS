# High Availability Web Server using Amazon Web Services (AWS)

## Project Overview
This project presents a scalable, secure, and fault-tolerant architecture for high-availability web services using Amazon Web Services (AWS). The solution is designed to handle varying traffic loads and leverages multiple AWS services to ensure scalability, performance, and security.

### Team Members:
- Savindu Wickramasinghe
- Nidula Mallikarachchi
- Thulith Hansana

## AWS Architecture
The architecture is built around the following key components:
- **Virtual Private Cloud (VPC):** A logically isolated section of AWS cloud with public and private subnets to ensure security.
- **Elastic Load Balancer (ELB):** Distributes incoming traffic across multiple EC2 instances to ensure high availability.
- **Auto Scaling:** Automatically adjusts the number of EC2 instances based on traffic demand.
- **Amazon S3:** Object storage for static content and file uploads.
- **Amazon CloudFront:** A Content Delivery Network (CDN) that speeds up content delivery globally.
- **Amazon DynamoDB:** A NoSQL database for storing structured data, including user information and file metadata.
- **AWS Lambda:** Serverless functions for event-driven processing.
- **Amazon Rekognition:** For image and video content moderation.
- **Amazon Elemental MediaConvert:** For media transcoding.
- **Amazon Route 53:** DNS service to manage traffic routing.
- **Amazon CloudWatch:** Monitoring service for resource utilization and operational health.

### Additional AWS Services Used
- **Amazon Cognito:** User authentication and access control.
- **AWS Identity and Access Management (IAM):** Fine-grained access control for AWS services.
- **AWS Shield and AWS WAF:** Protection against DDoS and common web vulnerabilities.
- **Amazon SQS:** Asynchronous message queuing for decoupling services.

## Key Features
- **Scalability:** The architecture uses Auto Scaling to dynamically scale resources based on traffic. AWS Lambda and SQS further enhance the ability to handle peak loads efficiently.
- **Security:** AWS Shield, WAF, and IAM policies protect the infrastructure. Cognito provides secure user authentication.
- **Performance Optimization:** CloudFront and ElastiCache are used to cache content closer to users and reduce latency.
- **Cost-Effectiveness:** The architecture is designed to balance performance and cost, utilizing a pay-as-you-go model and cost-saving AWS services like DynamoDB and Lambda.

## UML Diagrams
The following UML diagrams explain the flow of file uploads, downloads, and streaming:
1. **Request Pattern Diagram:** Shows user interaction with the web server and how requests flow through the architecture.
2. **File Upload Sequence:** Outlines the process of file uploads through API Gateway, Lambda, S3, and MediaConvert.
3. **File Download Sequence:** Shows how files are retrieved and served to users.
4. **Streaming Sequence:** Explains the flow of streaming requests through Lambda and API Gateway.

## Performance, Reliability, and Security
- **Performance:** Achieved through content caching (CloudFront), load balancing (ELB), and distributed compute resources (Auto Scaling).
- **Reliability:** Multi-AZ deployments for EC2, S3, DynamoDB, and automatic failover mechanisms ensure high availability.
- **Security:** A layered approach to security using VPC, IAM, Cognito, WAF, and Shield, combined with CloudWatch monitoring and CloudTrail for auditing.

## Cost Analysis
- **Fixed Costs:** AWS Shield at $3,000 per month.
- **Variable Costs:** Include usage of S3, CloudFront, Cognito, WAF, and other AWS services, adding up to an estimated total monthly cost of $19,281.63.
- **Cost Optimization:** The design leverages serverless computing and automated scaling to minimize costs during low-traffic periods.

## Future Scalability
The architecture is designed to support future expansion, with plans to handle up to 960,000 users over the next three years by doubling the user base every 6 months. AWS services like Auto Scaling and Lambda ensure the system will scale seamlessly.

## Conclusion
This project delivers a robust, scalable, and secure AWS architecture for a high-availability web server, leveraging best practices in cloud architecture and AWS service integration.

## Acknowledgments
Special thanks to Mr. Tharindu Suraj and the academic staff at Swinburne University of Technology for their support.

