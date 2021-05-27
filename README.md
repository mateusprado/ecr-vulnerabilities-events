# AWS ECR Vulnerabilities events

This is about ECR images scan vulnerabilities events for Amazon Eventbridge.
It is a option to monitor and automate events collection.

You can create Rules on the Eventbridge using the JSON template for each severity and use SNS Topic, Lambda as destination for this event when a new vulnerability is discovered.

You can run the Cloudformation template to setup all(you'll just need to setup the subscription for the SNS Topic)

```bash
 aws cloudformation create-stack --stack-name ecr-scan --template-body file://cf.yaml
```

The Dockerfile.example is a template that you can use to simulate the event HIGH(yes the image that will be created contains a CVE), creating a repository on ECR and push a image to there.

#KeepItSimple