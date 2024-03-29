+++
title = "Creating your environment"
chapter = false
weight = 1
+++

{{% notice warning %}}
You are responsible for the cost of the AWS services used while running this workshop in your AWS account.
{{% /notice %}}

In order for you to succeed in this workshop, you will need to run through a few steps in order to properly setup and configure your environment. These steps will include provisioning some services, installing some tools, and downloading some dependencies as well. We will begin with [AWS Cloud9](https://aws.amazon.com/cloud9/). Technically, you should be able to complete many of the steps in these modules if you have a properly configured terminal. However, in order to avoid the *"works on my machine"* response you've surely experienced at some point in your career, I strongly encourage you to proceed with launching Cloud9.

{{% notice tip %}}
[AWS Cloud9](https://aws.amazon.com/cloud9/) is a cloud-based integrated development environment (IDE) that lets you write, run, and debug your code with just a browser. It includes a code editor, debugger, and terminal. Cloud9 comes prepackaged with essential tools for popular programming languages, including JavaScript, Python, PHP, and more, so you don’t need to install files or configure your development machine to start new projects.
{{% /notice %}}

### Deploy & Launch AWS Cloud9

   [Click here to deploy using CloudFormation template](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateUrl=https://s3-external-1.amazonaws.com%2Fcf-templates-1j43xivmsfaj5-us-east-1%2F2019248RHx-contrast-aws-workshop-cloud9.yaml&stackName=contrast-aws-workshop-cloud9&param_VPCstack=)

   - Create stack click, **Create Stack**
  
>The deployment process takes approximately 2-3 minutes to complete. In the meantime, you can review the [deployment guide](https://aws-quickstart.s3.amazonaws.com/quickstart-cloud9-ide/doc/aws-cloud9-cloud-based-ide.pdf) while you wait.

Once the installation is complete, go to Cloud9 within the console and click on **Open IDE** on the name that begins with WorkshopIDE.

Here is the AWS infrastructure we are going to build and use in this workshop:

### Clone the source repository for this workshop

Now we want to clone the repository that contains all the content and files you need to complete this workshop.

```bash
cd ~/environment && \
git clone https://github.com/aws-samples/aws-modernization-with-contrastsecurity.git
```

### Increase AWS Cloud9 disk/storage
```bash
cd ~/environment/modernization-devsecops-workshop/scripts
./resize.sh 50
```

