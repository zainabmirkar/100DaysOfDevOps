# CloudWatch

- Metric Types: CloudWatch Metrics can be categorized into two types: AWS service metrics and custom metrics.
- AWS service metrics: These metrics are automatically generated and collected by AWS services such as Amazon EC2, Amazon S3, Amazon RDS, and more. They provide insights into the performance and behavior of these services.
- Custom metrics: You can also create your own custom metrics and publish them to CloudWatch. This allows you to monitor specific data and events from your applications or other resources running on AWS.
- CloudWatch Metrics allows you to create alarms based on metric thresholds. Alarms can trigger actions, such as sending notifications via Amazon SNS (Simple Notification Service) or executing an AWS Lambda function.
- You can use the CloudWatch console to create graphs, dashboards, and custom metrics widgets.

# Cloudwatch alarms

- Here's how CloudWatch Alarms work:
- Metric Selection: You start by selecting a metric from CloudWatch Metrics or creating a custom metric. Metrics represent the numerical data points that you want to monitor, such as CPU utilization, network traffic, or request counts.
- Alarm Creation: Once you have selected a metric, you can create an alarm based on that metric. You define a threshold or a range of values that triggers the alarm. For example, you can set a threshold for CPU utilization at 80%. When the CPU utilization exceeds this threshold, the alarm is triggered.
- Actions: When an alarm is triggered, you can configure one or more actions to be performed automatically. Actions can include sending notifications via Amazon SNS (Simple Notification Service), executing an AWS Lambda function, or stopping or terminating an EC2 instance.
- Alarm States: CloudWatch Alarms have three states:
- OK: The metric is within the defined threshold range.
- ALARM: The metric has breached the threshold or is outside the defined range. This state triggers the defined actions.
- INSUFFICIENT_DATA: There is not enough data to determine the state of the metric.

# CLoudwatch Logs
- required  for troubleshooting
- by default no logs will go to cloudwatch
- you need to run a cloudwatch agent on ec2 to push the log files you want
- make sure iam permissions are correct






















