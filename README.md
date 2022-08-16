# Project: Lambda Function

> In this project we will be creating a Lambda fuinction on AWS Cloud9 IDE.

### Overview
#### What is AWS Lambda
> AWS Lambda is a new category of computing where business logic can be directly deployed to a production environment without thinking about servers. Another word for this is serverless or FaaS (Function As A Service). Some of the benefits of AWS Lambda include no servers to manage, continuous scaling, and billing at the sub-second level.

> Another benefit of AWS Lambda includes being part of an ecosystem designed to exploit the capability. Here are two examples of AWS Lambda. The first example is AWS Step Functions. They build upon AWS Lambda to create more sophisticated workflows like polling for a job to finish and performing an action. The second example is AWS DeepLens (a computer vision device). It uses AWS Lambda to serve out predictions. Finally, if you look closely, almost every service on AWS can utilize AWS Lambda.

> The AWS ecosystem allows Lambda functions to respond to events instead of constantly running. This is similar to a motion detector that turns on a light in the garage. The duration the light may run for could be only a few hours per year. If the light switch was manually triggered it is possible the light would be run constantly for 365 days in the year.

> The AWS Lambda ecosystem allows integration with other core services in AWS through triggers. An example of a trigger would be a movie file that is uploaded to Amazon S3 storage. An AWS Lambda function could be triggered that uses an AWS API to transcode the movie file to a different code or to add captioning.

#### Prerequisites:
- You should have a Cloud9 environment running already in a separate browser tab.
- You must have cloned the [Github repo](https://github.com/OloruntobiOlurombi/DevOps_Microservices.git) in the Cloud9 environment and navigate to the folder contaning the exercise code. 

```
# Clone the repo if not already
git clone https://github.com/[Your-username]/DevOps_Microservices.git
# Navigate to the folder contaning the exercise code
cd DevOps_Microservices/Lesson-1-Lambda-functions/wikipedia-query
```

<img width="848" alt="Screen Shot 2022-08-15 at 5 37 44 PM" src="https://user-images.githubusercontent.com/40290711/184759268-cbb8b002-4dc4-4165-9b52-270d0eac9af0.png">


#### Steps:
Now, you're ready to complete some code of your own and deploy a FaaS that reads information from a Wikipedia page.

##### Step 1: Create a new Lambda function

> Create a new Lambda function ***HelloWiki*** or ***wikipedia-2021*** using the ***sam init*** command. Choose the following options in the prompts that appear next:

<img width="678" alt="Screen Shot 2022-08-15 at 5 45 30 PM" src="https://user-images.githubusercontent.com/40290711/184760171-4f4d276f-5ae6-41d0-83e4-135210f2bc57.png">

<img width="847" alt="Screen Shot 2022-08-15 at 5 46 29 PM" src="https://user-images.githubusercontent.com/40290711/184760697-dd9576e3-7b95-435e-b6a8-eda6ed132e30.png">

##### Step 2: Update app.py

> Update app.py - Copy the code present in the wikipedia_lambda_exercise.py file and paste it into the HelloWiki/hello_world/app.py file. There are some simple ToDo items for you in the wikipedia_lambda_exercise.py file. If you need help, you can refer/copy the wikipedia_lambda_solution.py code.

<img width="847" alt="Screen Shot 2022-08-15 at 5 46 29 PM" src="https://user-images.githubusercontent.com/40290711/184762959-5a8e3439-4aaa-46cc-a752-0834e37ab9e0.png">

##### Step 3: Update requirement.txt

> Update requirement.txt - Edit the HelloWiki/hello_world/requirement.txt file to include the depdendencies needed by the new application.

```
requests
wikipedia
```
##### Step 4: Create a virtual environment and install dependencies

```
cd HelloWiki/hello world 
python3 -m venv ~/.wiki
source ~/.wiki/bin/activate
python3 -m pip install -r requirements.txt
```
<img width="848" alt="Screen Shot 2022-08-15 at 5 57 54 PM" src="https://user-images.githubusercontent.com/40290711/184766651-a1ffe2e0-2c35-4387-9dac-3229350945c8.png">

##### Step 5: Create payload.json 

> Create ***payload.json*** file - Create a test payload (JSON) in the HelloWiki/ Lambda function directory, that will pass an entity as a request to your function.

```
{    
  "entity":"twitter"
}
```

##### Step 6: Build the application

```
# Check the HelloWiki/README file instructions
# Assuming you have updated the app.py, and requirement.txt 
# Assumnig you have created the  HelloWiki/payload.json file
# Ensure that you are in the HelloWiki/ directory
sam build
```
> The command above will Dockerize the Lambda function in the Cloud9 environment. You can view the [Application-name]/hello world/app.py file to see the expected output when you'll run the app.

##### Step 7: Run the application locally in the Cloud9 environment:

```
# Ensure that you are in the HelloWiki/ directory
sam local invoke -e payload.json
```

<img width="848" alt="Screen Shot 2022-08-15 at 6 05 03 PM" src="https://user-images.githubusercontent.com/40290711/184770204-4d2d5390-a1f1-4b07-8af8-0c7963d5a893.png">

##### Step 8: Deploy the app to an ECR image repository

Further, you can deploy the app to the ECR image repository. After deployment, you'd see the Lambda function in the AWS explorer panel.

```
sam deploy --guided
```
<img width="1438" alt="Screen Shot 2022-08-15 at 6 08 09 PM" src="https://user-images.githubusercontent.com/40290711/184773022-84a00f67-45b2-4f50-a5f5-feb775597f1b.png">

# The End

