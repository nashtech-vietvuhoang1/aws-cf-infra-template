# aws-cf-infra-template
AWS CloudFormation Infrastructure Template

## Using Rain

### Reference

- [AWS CloudFormation Rain](https://github.com/aws-cloudformation/rain)
- [AWS CloudFormation Template](https://github.com/aws-cloudformation/aws-cloudformation-templates)

### Generate CloudFormation

```bash
rainpkg
```
## CloudFormation Execution

### CloudFormation Validate

```bash
aws cloudformation validate-template --template-body file://.tmp/main-stack.yaml
```

### CloudFormation Create

```bash
aws cloudformation create-stack --template-body file://.tmp/main-stack.yaml --stack-name <your-stack-name> --capabilities CAPABILITY_IAM,CAPABILITY_AUTO_EXPAND 
```
