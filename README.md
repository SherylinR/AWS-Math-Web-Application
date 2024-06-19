# Math Web Application with AWS

This project demonstrates how to design and build a simple web application using five different AWS services: Amplify, Lambda, IAM, API Gateway, and DynamoDB. The documentation covers the roles and integration of each service, resulting in a fully functional math web application.

### AWS Services Used

- **AWS Amplify**
- **AWS Lambda**
- **API Gateway**
- **DynamoDB**
- **IAM**

## Prerequisites

- A text editor (such as Notepad or Notepad++)
- An AWS account and access to the Console. NOTE: Administrator permissions are required.

## Project Overview

Here’s all the code needed to build the application:

- index-ORIGINAL.html
- PowerOfMathFunction - Lambda-ORIGINAL.txt
- Execution Role Policy JSON.txt
- PowerOfMathFunction - Lambda-FINAL.txt
- index.html

## Implementation Details

### Web Application Hosting

The project begins with the creation of a simple `index.html` file using a text editor. This HTML file is then launched as a web application using AWS Amplify. The steps include:

**AWS Amplify Setup:**
   - Created a new application in AWS Amplify.
   - Uploaded the `index.html` file.
   - Hosted the web application, providing a specific domain URL for access.

### Lambda Function for Math Operations

Since the web page involves some math functions, an AWS Lambda function is created to handle these operations:

**Lambda Function Creation:**
   - Used Python to write a simple Lambda function that implements the required math operations.
   - Deployed the Lambda function.

### API Gateway Integration

To invoke the math function created by Lambda, an API Gateway is used to create a new REST API:

**API Gateway Setup:**
   - Created a new REST API.
   - Configured a POST method to send data to the Lambda function.
   - Enabled CORS in the API to allow access from the web application hosted on AWS Amplify.

### Data Storage with DynamoDB

Results of the math operations need to be stored, so a DynamoDB table is created:

1. **DynamoDB Table Creation:**
   - Created a new DynamoDB table to store math results.

2. **IAM Policy for DynamoDB Access:**
   - Created a new IAM Policy, specifying the ARN of the DynamoDB table.
   - Attached the policy to the Lambda function to grant access to the DynamoDB table.

3. **Lambda Function Update:**
   - Updated the Python code in the Lambda function to store the results in the DynamoDB table by importing the table details.

### Final Integration

The final step is to connect the web application hosted in AWS Amplify with the API Gateway:

**Web Application Update:**
   - Updated the `index.html` file to specify the API Gateway Endpoint.
   - Made necessary UI changes to accommodate the API integration.
   - Redeployed the updated web application in AWS Amplify.

This integration allows the web application to invoke the math functions through the API Gateway, process the results with the Lambda function, store the results in DynamoDB, and display the final output on the web page.

## Project Build Workflow
I started by creating a simple `index.html` page using a text editor. To launch it as a web application using my AWS account, I utilized AWS Amplify. I created a new application in AWS Amplify and uploaded my `index.html` file. This allowed the page to be hosted as a new web app with a specific domain URL for access.

Since my web page involves some math functions, I used AWS Lambda to create a new, simple Lambda function using Python to implement the required math operations. After developing the function, I deployed it in Lambda. To invoke the math function created by Lambda, I used API Gateway to create a new REST API. As users need to send data to the Lambda function, I created a POST method in our API and integrated it with our math Lambda function. Additionally, I enabled CORS in our API to ensure our web application running on AWS Amplify can access the Lambda function.

To store the math results, I created a new DynamoDB table. To give the Lambda function access to DynamoDB, I created a new IAM Policy by specifying the ARN of the table we launched. This policy was added as an inline policy to the Lambda function, granting it access to the specific DynamoDB table. Subsequently, I updated the Python code in the Lambda function to store values in the DynamoDB table by importing all the necessary table details.

Finally, to establish a connection between our web app hosted in AWS Amplify and our API, I updated the `index.html` file to specify our API Gateway Endpoint, along with making all the necessary UI changes. After making these updates, I redeployed the application in AWS Amplify. The final web app now successfully implements the math function, with the results being displayed on the web page and stored in DynamoDB.

## Sample Images
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/Overview.png)
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/Resources.png)
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/lambda.png)
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/Deployments.png)
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/DynamoDB.png)
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/Lambda%20Funtion.png)
![alt-text](https://github.com/SherylinR/AWS-Math-Web-Application/blob/main/images/Output%20-%201.png)


---
