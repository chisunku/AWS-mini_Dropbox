# AWS-mini_Dropbox
- Creating a 3-tier web application that the users can use upload, download and store their files in.
- This project is designed and developed using various AWS services with cost effective solutions. 

### URL (expired): https://drop.chinmayisunku.ml/
### [Demo](https://drive.google.com/file/d/1gNGw1dDhrfeIpnDEJG2EdrAhVGk_2FI4/view?usp=share_link)

## Instruction to run:
- Software required: SpringBoot and React
- Clone both the repo 
- To run the backend, run the main file, [FileStorageServiceApplication.java ](https://github.com/chisunku/AWS-mini_Dropbox/blob/main/backend/src/main/java/com/example/dropbox/FileStorageServiceApplication.java) 
- To run frontend:
  - npm install (to install the node_module)
  - npm start (to start the application)

## AWS resources used:
- **S3**: Amazon S3 is an object storage service provided by AWS. S3 is used in our application to store the images user uploads for the blogs. The bucket is replicated for disaster recovery. S3 bucket policy are in place keeping in mind costing.
- **CloudFront**: CloudFront is the CDN operated by AWS. We used this to access the S3 bucket objects.
- **EC2**: EC2 is a compute service provided by Amazon. EC2 is used to deploy the application. EC2 is made scalable by attaching auto scale groups. Made available to other AZ for disaster recovery.
- **DynamoDB**: DynamoDB is a NoSQL service provided by AWS. We used DynamoDB to store the user information and restaurants information. This information is used later to fetch the blogs. The restaurants DB is used for restaurants recommendation.
- **Route53**: Route53 is the DNS service provided by AWS. We used it to redirect our domain to our application. This makes it easy for the users to access the web application.
- **Lambda**: AWS Lambda is a serverless compute platform. We used Lambda functions for 2 tasks. One function was to automatically confirm the users once they login. The second function was to send email to the admin when the user uploads blogs.
- **Cognito**: AWS Cognito is user authentication service provided by Amazon. We have used Cognito to keep track of the users for the application.
- **CodePipeline**: AWS CodePipeline is a CI/CD service provided by Amazon. We integrated CodePipeline with github to rebase the updates in the application code.
- **SNS**: SNS is a notification service provided by AWS. We have used this to notify when objects are uploaded into the S3 bucket.

## Note: 
- AWS resources set-up in the document uploaded. 
- To run the application successfully add the AWS credentials in the [application.yml](https://github.com/chisunku/AWS-mini_Dropbox/blob/main/backend/src/main/resources/application.yml)
