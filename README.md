Email Sentiment Analyzer (AWS POC)

Business Problem:
As part of procurement and sales, we used to get hundreds of customer support emails.  
It was difficult to prioritize not satisfied customers manually and respond on time.

Solution:
I built a POC on AWS that:
- Uses S3 or SES to receive emails
- Triggers a Lambda function on new email
- Uses Comprehend to detect sentiment (Positive, Neutral, Negative)
- Sends alert via SNS for Negative/Angry emails

Architecture Flow:
- Customer sends support email  
- Email stored in S3 (simulated SES)  
- Lambda triggers on upload  
- Comprehend analyzes email text  
- If Negative → SNS sends alert  
- All results stored in CloudWatch logs

AWS Services Used:
S3, Lambda, Comprehend, SNS, IAM Roles, CloudWatch

Business Value:
- Alerts for angry customers in real-time  
- Speeds up support response  
- Helps prioritize and tag incoming emails  
