# AWS CloudFormation VPC Nested Stack Template

This AWS CloudFormation template sets up a Lambda function, an SNS topic, and a scheduled event to trigger the Lambda function. The Lambda function sends a response back when invoked.

## Parameters

- **LambdaRate**: Specifies the rate at which the Lambda function is triggered. Default: "cron(15 10 * * ? *)".
- **EnvironmentName**: Selects the environment, with options for 'prod' or 'dev'. Default: prod.

## Conditions

- **Condition**: Determines whether to add SNS as a destination for success and failure messages.

## Resources

- **LambdaRole**: IAM Role for the Lambda function.
- **SNSLambdapolicy**: IAM Policy for SNS attached to the Lambda role.
- **LambdaFunction**: AWS Lambda Function.
- **version**: Lambda Function Version.
- **LambdaSNSPermission**: Permission for Lambda events.
- **SNSTopic**: SNS Topic for Lambda.
- **asyncconfig**: Event Invoke Configuration for Lambda.
- **LambdaSchedule**: Schedule for the Lambda function.
- **LambdaSchedulePermission**: Permission for Lambda events triggered by a schedule.

## Outputs

- **MyTopicArn**: Arn of the created SNS Topic.

## Instructions

1. Replace the code in `ZipFile` under `LambdaFunction` with your actual Lambda function code.
2. Modify parameters and configurations as needed in the CloudFormation template.
3. Deploy the stack using the AWS CloudFormation console or CLI.

## License

[MIT License](LICENSE)

---

For more information,
