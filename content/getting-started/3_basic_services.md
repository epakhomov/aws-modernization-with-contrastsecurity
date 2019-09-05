+++
title = "Setup Basic Services"
chapter = false
weight = 3
+++

### Create Underlying VPC Infrastructure

```bash
aws cloudformation create-stack --stack-name ContrastSecurityWorkshopVPC --template-body file:///$(pwd)/cfn/aws-workshop-vpc.yaml --capabilities CAPABILITY_NAMED_IAM
```

### Check VPC Resource Creation Status

```bash
aws cloudformation wait stack-create-complete --stack-name ContrastSecurityWorkshopVPC
```