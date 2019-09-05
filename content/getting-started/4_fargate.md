+++
title = "Deploy ECS Fargate Service"
chapter = false
weight = 4
+++

### Configure ECS Stack Parameters

Add Contrast keys from contrast_security.yaml to cfg/contrast-aws-workshop-ecs-parameters.json file.

### Create ECS Resources

```bash
aws cloudformation create-stack --stack-name ContrastSecurityWorkshopECS --template-body file:///$(pwd)/cfn/contrast-aws-workshop-ecs.yaml --parameters file://$(pwd)/cfg/contrast-aws-workshop-ecs-parameters.json --capabilities CAPABILITY_NAMED_IAM
```

### Check ECS Resource Creation Status

```bash
aws cloudformation create-stack-complete --stack-name ContrastSecurityWorkshopECS
```

### Getting outputs

You will need at least the Load balancer DNS to be able to access WebGoat. You can do it with this command:

```bash
aws cloudformation describe-stacks --stack-name ContrastSecurityWorkshopECS
```

