# AWS CDK TypeScript Starter

This is a basic AWS CDK project written in TypeScript that creates three S3 Buckets using various constructs. It also includes a CloudFormation output construct to log the name of one of the S3 Buckets when deploying.

## Prerequisites

Before you begin, make sure you have the following prerequisites installed:

_Node.js (v14 or later)_
_AWS CDK Toolkit (Command Line Interface)_
_AWS CLI (Command Line Interface) configured with your AWS credentials_
_Getting Started_

## Clone the repository:

`git clone https://github.com/yourusername/aws-cdk-typescript-starter.git`
Navigate to the project directory:

`cd aws-cdk-typescript-starter`
Install the project dependencies:

`npm install`

# Project Structure

lib/cdk-starter-stack.ts: The CDK stack definition file where the S3 Buckets are created using various constructs.
bin/cdk-starter.ts: The entry point for CDK app.
cdk.json: Configuration file for CDK app.
package.json and package-lock.json: Node.js project configuration files.
Usage

## Configuration

### CloudFormation Parameter

This project includes a CloudFormation parameter named duration which constrains the duration of files on one of the S3 Buckets (MyL2Bucket). You can customize the default, minimum, and maximum values for this parameter in the lib/cdk-starter-stack.ts file.

### CloudFormation Output

There are two different stacks being created:
PhotosStack and PhotosHandlerStack:

PhotosStack: Creates the photos-bucket S3 Bucket - Outputs Bucket reference

PhotosHandlerStack: Imports Bucket reference and executes a lambda function

There is a Bucket Tagger that uses CDK Aspects to tag all S3 Buckets with a level: test key value pair

A CloudFormation output named MyL2BucketName is defined in the stack. It logs the name of the MyL2Bucket when the stack is deployed. You can access this value after deployment.

### Author

Arthur Rabelo

### Acknowledgments

Thanks to the AWS CDK community for their valuable resources and documentation.
