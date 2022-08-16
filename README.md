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


