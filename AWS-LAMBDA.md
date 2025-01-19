# Automate start and stop of EC2 Instance using the AWS Lambda.
# Lambda will contain the necessary function in order to stop and start your EC2 Instances.
# To trigger those functions and setup the time slot for automation we will use the Amazon EventBridge.

# steps for Lab implementation
  1) EC2 Instance need to be tagged, for example set the tag 'project' with the value of 'uat'.
  2) create IAM Policy (here we have used Json file provided in course for creating policy) and IAM Role to allow Lambda access to your EC2 Instances with the permissions start and stop those instances.
  3) create the Lambda function which will perform the start and stop of your EC2 Instances. (here we have used the python code in Lambda which was provided in course)
       - deploy the code
       - go to configuration -> Environment variables
       - add environment variable
       - we need to put key as "DEFAULT_TAGS" and value as "tag:project=uat" (this the same tagb we have put on the EC2 instance tags) (the DEFAULT_TAGS comes from the code)
       - again key as "LOG_LEVEL" and value as "INFO".
       - now to test the lambda function we need to create the new test case
       - test case will be written in Json format (below written code will stop the EC2 Instance having the same tags as above defined.
               { "action": "stop"
                 "tags": "log:project=prod"   #we can also define tags here in this function if not defined in the environment variables.
               }  
  4) Configure an EventBridge scheduled event to trigger the Lambda function at the designated schedule to perform the start and stop of your EC2 instances.
       - we will create two new rules EC2startevent and EC2endevent.
       - define the function in Json format it has to perform.
               { "action": "stop/stop"
               }
       - schedule and time slot will be as per the cron format.
    
NOTE- https://repost.aws/knowledge-center/start-stop-lambda-eventbridge (THIS IS THE PROPER DOCUMENTATION OF AWS)
     
