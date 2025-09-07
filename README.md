Email Sentiment Analyzer (AWS POC)

Problem Statement:
Reading and replying to customer support emails manually was slow and inconsistent in tone detection.

Solution:
Created a POC on AWS using:
- SES to receive support emails.
- S3 to store raw `.eml` files.
- Lambda to extract content and run sentiment analysis.
- Comprehend to detect emotions (Positive, Negative, etc.).
- DynamoDB to store structured data like email, tone, subject.

How It Works:
1. Email received via AWS SES.
2. Stored in S3 automatically.
3. SNS triggers a Lambda.
4. Lambda reads the email content.
5. AWS Comprehend detects the tone.
6. Final result saved in DynamoDB.

Architecture Diagram:
(see image below)

Skills Used:
SES, S3, Lambda, Comprehend, DynamoDB, IAM Roles, SNS

Business Impact:
- Automatically tags customer mood (Positive/Negative/Neutral)
- Faster and more accurate
