# alexa-nodejs-template

The purpose of this project is to make it as easy as possible to set up a new Hello World Alexa Skill that runs as a nodejs Lambda function on AWS.

## Getting Started / Installation Instructions

1) Create an [AWS Account](http://aws.amazon.com/).
2) On Mac/Linux, `pip install awscli`. Windows, download executable from [here](http://aws.amazon.com/cli/).
2.5) Configure the aws CLI with `aws configure`
3) Make sure [NodeJS](https://nodejs.org/) is installed.
4) Go to the [Amazon Developer Portal](https://developer.amazon.com/edw/home.html). Click "Get Started" with Alexa Skills Kit.
5) In a separate tab, go to the [Lambda Function Portal](https://console.aws.amazon.com/lambda/home?region=us-east-1#/functions) on AWS.
6) Go through the steps to create a new Lambda function - skip the blueprint step, choose a name for your function (save this for later), and write down the Application ID. You'll need it later. Then select "Upload a .ZIP file" under "Lambda function code".
7) Now you'll need to upload a zip file to get started with code for your Lambda function. Switch over to your terminal where you checked out this project, and do an `npm install`.
8) Run `gulp zip` to generate a zip file in the ./dist folder.
9) Switch back to the browser on Lambda and select the "archive.zip" under Upload.
10) Choose a role for your Lambda function - either create a Basic execution role or use a one you previously set up.
11) Click "Next" and then "Create Function"
12) Switch to the "Event Sources" tab and add an event source type for "Alexa Skills Kit"
13) Switch back to the Alexa Developer Console tab and choose "Add a New Skill"
14) Choose a Name and Invocation Name for your skill (see docs for more info) - or just Use "Hello World" and "Greeter" to follow the Hello World example.
15) Under "Intent Schema", copy the contents of ./speechAssets/IntentSchema.json. Under "Sample Utterances", do the same with SampleUtterances.txt.
16) Click Next, then switch over to the Lambda Function tab and copy the value for ARN which should be in the top right corner of the page when viewing your Lambda Function.
17) Paste this in the "Configuration > Endpoint" field of the Alexa developer console and hit "Next".
18) Open src/config.js and replace the appropriate values with Lambda ARN, Lambda Function Name, Amazon App ID (found [here](https://developer.amazon.com/edw/home.html#/skill/amzn1.echo-sdk-ams.app.b78331c4-e09e-40dc-86be-71a17c1db162/info)), region (defaults to us-east-1), and skill title.
19) At this point you should be able to test your skill with your Amazon Echo by using the phrase you configured in the Invocation Name.

## Testing
TODO using gulp test



