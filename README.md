# Serverless Website

This project demonstrates how to deploy a secure website using a serverless framework on AWS. 
The website includes functionalities for user authentication, file uploads, and storing data in a database, all implemented with AWS serverless services for a minimal cost and maintenance.

Services used (so far): 
   - API Gateway
   - Lambda
   - S3
   - DynamoDB
   - Cognito

## 1. Project Overview
### 1.1. Goal
The goal of this project is to deploy a secure and scalable serverless website with the following features:
- Secure authentication using AWS Cognito for user management.
- File uploads (e.g., images) to an S3 bucket.
- Storage of data and metadata in a DynamoDB table.
- Publishing notifications using AWS SNS when new data is created (TODO).
- RESTful API endpoints built with AWS Lambda functions.
- CORS support for client-side requests.
- Networking (TODO)

### 1.2. Why Serverless?
The serverless architecture allows for automatic scaling, reduced infrastructure management, and a pay-per-use pricing model.
By using AWS services like Lambda, S3, DynamoDB, and Cognito, this project can deliver a robust and scalable solution without needing to manage servers.

## 2. Architecture
### 2.1. AWS Services Used
- **AWS Lambda**: For running backend code without provisioning servers.
- **Amazon API Gateway**: To expose RESTful APIs that connect to Lambda functions.
- **Amazon S3**: For storing uploaded files such as images.
- **Amazon DynamoDB**: To store metadata and information about uploaded files.
- **Amazon Cognito**: For user authentication and authorization.
- **Amazon SNS (Simple Notification Service)**: For publishing notifications after new data is created.
- **AWS IAM**: For managing access to AWS services securely.
- **Networking**: (TODO)

### 2.2. Application Workflow
1. **User Authentication**: The user signs in using AWS Cognito. JWT tokens are used for authentication.
2. **File Upload**: Authenticated users can upload files (e.g., images) through the web interface.
3. **Data Processing**:
   - The uploaded file is processed and stored in an S3 bucket.
   - Metadata about the file (e.g., filename, associated user, etc.) is stored in a DynamoDB table.
4. **Notifications**: An SNS notification is sent when a new file is uploaded.

## 3. Setup Instructions
### 3.1. Prerequisites
- **AWS Account**: You'll need an AWS account to deploy the resources.
- **Node.js** and **npm**: Ensure you have Node.js and npm installed on your machine.
- **Serverless Framework**: Install the Serverless Framework CLI globally using `npm install -g serverless`.
- **Python**: Python is required for Lambda development and packaging dependencies.

### 3.2. Installation Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/vascodpm/secure_serverless_website.git
   cd serverless-website

## 4. Notes
The YAML configuration (serverless.yml) was developed by me for this project.
The frontend and backend code were adjusted from this repository: https://github.com/aussiearef/.

## 5. Usage
Once deployed, the application can be accessed via the API Gateway endpoint. Users will be able to:

Sign up and log in using Cognito.
Upload files, which will be stored in S3.
Submit data, which will be saved in DynamoDB.


