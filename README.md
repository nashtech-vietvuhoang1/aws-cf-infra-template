# aws-cf-infra-template
AWS CloudFormation Infrastructure Template

## Using Rain

### Reference

- [AWS CloudFormation Rain](https://github.com/aws-cloudformation/rain)
- [AWS CloudFormation Template](https://github.com/aws-cloudformation/aws-cloudformation-templates)

## Before execution

CloudFormation requires a S3 bucket to store tempolary template files

### CloudFormation Validate

```bash
verify <stack-file>
```

### CloudFormation Deploy

```bash
./deploy <stackname> <deployment-S3-bucket-name> <region> <deployment-environment>
```
