# Setup Instructions
This is an instruction guide for our demo use case which is:- **Serverless website.**   
The problem can be replicated using terminal or the AWS console. However, for tutorial purposes and quick understanding, we will demonstrate using the AWS Lambda console in a browser.
## Pre requisites
+ An [Amazon AWS](https://aws.amazon.com/) account with administrative access.
## Configuration
### 1. Configuring the Lambda function
+ Log in to you AWS console using any standard browser.
+ Navigate to `Services-> Compute-> Lambda` to open the Lambda dashboard.
+ Click on **_Create Function_**
+ Select **_Author from scratch_** tab (we'll do everything from scratch! (¬‿¬) )
+ Configure the options as shown in the figure below and click **_Create Function_**:  
Here, we select `Runtime=python3.6` since the lambda function we'll write is in python3. The function is named **myLambdaFunction**.

![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig1.PNG)

Next, we'll define the lambda function and add an API to trigger lambda function.
### 2. Define Lambda Function
+ Click on the **_myLambdaFunction_** field and scroll down to configure.  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig4.PNG)
+ Copy and paste the entire [lambda_function.py](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/f295c5ba7a765de366677d598548d598d9f7234a/src/lambda_function.py#L1) into the default `lambda_function.py` shown on the aws console. The result should look like this:  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig5.PNG)  
 
The lambda function is now defined and only thing left is to add an API to trigger the lambda function.
### 3. Configure API Gateway Trigger
+ Scroll up and select `Designer-> Add Trigger-> API Gateway` that will add an API gateway trigger for the lambda function.  
  
 ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/addAPI.gif)
+ Scroll down to configure the API gateway. We'll create a new API named **LambdaAPI** as shown below:  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig3.PNG)
 + Click **_Add_** to finish configuration of API gateway.

All the necessary configurations for the lambda function are done. Click on **_Save_** at the top to save all the configurations.

### 4. Additional configiuration for API Gateway
+ Our client will require an invocation url to make a _GET_ call to the serverless lambda function. 
+ Navigate to `Services-> Networking & Content Delivery-> API Gateway`. You will find the **LambdaAPI** already existing there. Delete the **ANY** method and create a **GET** method.   
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/createGetMethod.gif)
+ Configure the GET method as follows and click **_Save_**:  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/lambdaConfig10.PNG)
+ You get an invocation url after saving, modify it in [index.html](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/cee0c3f098e81e741ad7f4631dc3e650219c9a64/src/index.html#L11) to pass it as the second argument.
## Testing
Now we are all set to see our website in action. Run the modified `index.html` file in a browser and click on the **_Click me_** button to see the result from the lambda function.  
  
  ![](https://github.com/AnkurSaxena135/AWS-Lambda-TechTalk/blob/master/src/material/success.gif)
  
And Viola! we have our first serverless website up and running!! 
