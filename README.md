# AWS-Lambda-TechTalk

## Team Members:
| Name | UnityId |
|---------------------|-------|
| Zachery Thomas | zithomas | 
| Vikas Pandey | vrpandey | 
| Prerit Bhandari | pbhanda2 |
| Ankur Saxena | asaxena3 | 

## [Screencast](https://youtu.be/j4rjmO48iKY) | [Presentation](https://docs.google.com/presentation/d/1TZOdpt8iu-oLkwhWfXZ2b0opiImOty70rzY3eKUz14g/edit?usp=sharing) | [Setup Instructions](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/README.md)

## Introduction to AWS Lambda
### What is AWS Lambda
AWS Lambda is a serverless compute service by Amazon. It lets you run code without you having to provision or manage servers. 

### How does it work?
![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/howlambda.PNG)
+ The developer codes the lambda function and specifies the runtime environment. 
+ These functions can be triggered through preconfigured APIs, S3 Buckets, DynamoDB and various other methods.
+ Once a function is triggered, AWS runs it for you and you only pay for the number of miliseconds your function runs.
+ Job done, no servers - no hassle!

### Canon Use Cases [1]

#### 1. Real-time File Processing
![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/uc1.PNG)
#### 2. Extract-Transform-Load
![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/uc2.PNG)
#### 3. Web Applications
![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/uc3.PNG)
#### 4. Mobile Backends
![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/uc4.PNG)

### Other tools like AWS Lambda
![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/similartools.png)
### Should I Lambda or should I not? [2]
+ **Why I should?**
    + Reduced time to market and quicker software release.
    + Lower operational and development costs.
    + A smaller cost to scale – there is no need for developers to implement code to scale and administrators do not need to upgrade existing servers or add additional ones.
    + Works with agile development and allows developers to focus on code and to deliver faster.
    + Fits with microservices, which can be implemented as functions.
    + Reduces the complexity of software.
    + Simplifies packaging and deployment and requires no system administration.
+ **Why I shouldn't?**
    + Serverless is not efficient for long-running applications.
    + Vendor lock-in.
    + Introduces additional overhead for function/microservice calls.
    + In practice, it takes some time for a scalable serverless platform to handle a first request by your function.
    + No out-of-the-box tools to test functions locally.

### References
1 [AWS lambda documentation](https://aws.amazon.com/lambda/)  
2 [Serverless pros-cons](https://devops.com/go-serverless-pros-cons/)
