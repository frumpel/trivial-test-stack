# trivial-test-stack

This stack will create an S3 bucket. Name of the bucket is defined by a parameter

Example invocation

```
aws cloudformation create-stack \
  --stack-name trivial-test \
  --template-body file://template.yaml 
  --parameters file://params.json 

aws s3 ls 

aws cloudformation delete-stack --stack-name trivial-test
```

Useful links for later

* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stacks-quick-create-links.html

Testing - this will break as API location changes

[Launch Stack](https://lze585tezf.execute-api.us-west-2.amazonaws.com/Prod/?templateUrl=https://raw.githubusercontent.com/frumpel/trivial-test-stack/main/template.json&param_BucketName=testing-only-do-not-use&param_BucketNameErrorUndefinedParam=testing-only-do-not-use)

