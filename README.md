# Trivial test stack for AWS CloudFormation

This stack will create an S3 bucket in AWS. The name of the bucket is defined by a parameter.

## Invoking via CLI

Example invocation. This presumes that you have installed the AWS CLI and configured access credentials:

```
aws cloudformation create-stack \
  --stack-name trivial-test \
  --template-body file://template.yaml 
  --parameters file://params.json 

aws s3 ls 

aws cloudformation delete-stack --stack-name trivial-test
```

## Invoking using the AWS CloudFormation console

To launch this stack directly from the AWS console, make sure you are logged into the AWS console in this browser. Then use this button, created by [stacklauncher.cloud](https://www.stacklauncher.cloud):

### Using JSON template without parameters

This button will use the content of `template.json`. Any required parameters will have to be defined in the AWS console:

[![Launch Stack in AWS](https://www.stacklauncher.cloud/assets/icons/button-aws-18.png)](https://api.stacklauncher.cloud?templateUrl=https://raw.githubusercontent.com/frumpel/trivial-test-stack/main/template.json)

### Using YAML template without parameters

This button will use the content of `template.yaml`. Any required parameters will have to be defined in the AWS console:

[![Launch Stack in AWS](https://www.stacklauncher.cloud/assets/icons/button-aws-18.png)](https://api.stacklauncher.cloud?templateUrl=https://raw.githubusercontent.com/frumpel/trivial-test-stack/main/template.yaml)