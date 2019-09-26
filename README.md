## Reference
- [AWS API Gateway With Cognito Authorization-2017](https://www.youtube.com/watch?v=IiWyPb389UU)


## Step 1: Create Cognito user pool
Get App client id and App client secret


## Step 2: Create Lambda functions and role/permission for earch of function
- DemoPreSignUp (Role)

- DemoSignIn (Role)

- DemoPing (Role DemoPing)


## Step 3: Create API gateway
- API: DemoSignIn

Resource: authenticate

Method: POST, integrate with lambda function DemoSignIn

- API: DemoPing

Resource: ping

Method: GET, integrate with lambda fuction DemoPing

Create Authorizer for this API
name: CognitoAuthorizer
type: Cognito
Cognito User Pool: Created at step 1
Token Source: Authorization     # the auth header

Apply Authorizer to api's auth



