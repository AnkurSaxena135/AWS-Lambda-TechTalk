# Setup Instructions
This is an instruction guide for our demo use case which is:- **Serverless website.**   
The problem can be replicated using terminal or the AWS console. However, for tutorial purposes and quick understanding, we will demonstrate using the AWS Lambda console in a browser.
## Pre requisites
+ An [Amazon AWS](https://aws.amazon.com/) account with administrative access.
## 1. Configuring the Lambda function
+ Log in to you AWS console using any standard browser.
+ Navigate to `Services-> Compute-> Lambda` to open the Lambda dashboard.
+ Click on **_Create Function_**
+ Select **_Author from scratch_** tab (we'll do everything from scratch! (¬‿¬) )
+ Configure the options as shown in the figure below and click **_Create Function_**:  
Here, we select `Runtime=python3.6` since the lambda function we'll write is in python3. The function is named **myLambdaFunction**.

![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig1.PNG)

Next, we'll define the lambda function and add an API to trigger lambda function.
## 2. Define Lambda Function
+ Click on the **_myLambdaFunction_** field and scroll down to configure.
+ Copy and paste the entire [lambda_function.py](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/f295c5ba7a765de366677d598548d598d9f7234a/src/lambda_function.py#L1) into the default `lambda_function.py` shown on the aws console. The result should look like this:  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig5.PNG)
## 3. Configure API Gateway Trigger
+ Select `Designer-> Add Trigger-> API Gateway` that will add an API gateway trigger for the lambda function.  
  
 ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/addAPI.gif)
+ Scroll down to configure the API gateway. We'll create a new API as shown below:  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig3.PNG)
 + Click **_Add_** to finish configiuration of API gateway.
