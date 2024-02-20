# Componenets of CW

## dashboards:
- using console, cli or PutDashboard Api you can create visual widgets. you can share with users which do nt have access to aws account as well
  
## CW metrics and anomaly detection :
- they enable you to monitor a specific element or resource over a period of time while tracking data points. free monitoring every ```5 minutes``` for ec2 and u can enable ```detailed monitoring for every 1 minute```. you can also create   ```custom metrics``` (cm are regional)
### Anomaly detection
- When you enable anomaly detection for a metric, CloudWatch applies statistical and machine learning algorithms
- There are 2 types. 1)```Create anomaly detection alarms based on a metric's expected value.```
- 2)```When viewing a graph of metric data```, overlay the expected values onto the graph as a band. This makes it visually clear which values in the graph are out of the normal range.

 ### CW Alarms
- can configure sns when ec2 utilization falls below 75% causing it to come in alarm state
- 3 states ...  ```OK``` means the alarm is within the threshold... ```ALARM```  metric is in threshold state and ```INSUFFICIENT DATA``` means the alarm has just started or there is no enough data
- can be ```integrated with dashboards```


### eventbridge
- AWS EventBridge is a serverless event bus service provided by Amazon Web Services (AWS).
- ```events``` EventBridge allows you to define rules that match incoming events based on certain criteria. When a rule matches, it triggers the associated target.
- ```targets``` These are the services or components that respond to events. For instance, a Lambda function, an SNS topic, or a Step Functions workflow can be event targets.
- ```events``` Events are occurrences or changes in your AWS environment. This could be anything from a file being uploaded to an S3 bucket, a new item being added to a database, or a user signing in to your application.
- ```event bus``` component that receives the event. there is a default bus but you can create your own as well

### logs
- centralized location to house all your logs
- ```CloudWatch Logs offers two classes of log groups``` The CloudWatch Logs ```Standard log class``` is a full-featured option for logs that require real-time monitoring or logs that you access frequently. The ```CloudWatch Logs Infrequent Access log class``` is a new log class that you can use to cost-effectively consolidate your logs. ```The Infrequent Access log class``` is ideal for ad-hoc querying and after-the-fact forensic analysis on infrequently accessed logs.
- ```cw log insights``` With CloudWatch Logs Insights, you can interactively search and analyze your log data in Amazon CloudWatch Logs. You can perform queries to help you more efficiently and effectively respond to operational issues. CloudWatch Logs Insights generates visualizations for queries that use the stats function and one or more aggregation functions. For more information
- ```cw agent``` can collect logs fron ec2 or onpremise server consisting of windows or linux. these are additional metrics collected apart from the deafault metrics
- ```container insights``` Container Insights is specifically designed for monitoring and gaining insights into containerized applications, such as those deployed using Amazon ECS and EKS. also allows you to capture diagnostic data into how to resolve issues that arise within your container architecture. the monitoring and insight data can be analyzed at pod, node, task level

## Lambda insights
- helps to troubleshoot serverless apps
- just enable the ```enhanced monitoring``` in lambda 
