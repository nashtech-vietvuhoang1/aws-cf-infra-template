# aws-cf-infra-template
AWS CloudFormation Infrastructure Template

## Prerequisite

## AWS CLI

AWS CLI is required in this project, please install AWS CLI follow to this link [Install or update to the latest version of the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) 

> If you aleady have AWS CLI in your workspace (PC/Mac/VM), ignore this step

## AWS Credentials

Please make sure that you have an AWS Credentials with associated ACCESS_KEY and SECRET KEY on your workspace

```
aws configure
```

Following IAM Permissions is required:
- s3:PutObject 
- T.B.D

## S3 Bucket for storing tempolary template

S3 Bucket is required for storing tempolary template as reqirement of ```aws cloudformation package``` command

## EC2 Bastion Host KeyPair

a KeyPair should be prepared for Bastion Host initialization purpose 

### CloudFormation Validate

```bash
verify <stack-file>
```

### CloudFormation Deploy

```bash
./deploy <stackname> <deployment-S3-bucket-name> <region> <deployment-environment>
```

Example 

```bash
./deploy demo-cf demo-cf-dev-s3bucket ap-southeast-1 Dev demo-cf-dev-bastion-host-keypair
```

Using Environment variables:

```bash
STACKNAME=demo-cf \
S3_BUCKET=demo-cf-dev-s3bucket \
TARGET_ENV=Dev \
REGION=ap-southeast-1 \
BASTION_HOST_KEY_NAME=demo-cf-dev-bastion-host-keypair \
./deploy
```