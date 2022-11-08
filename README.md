# Serverless ActivityPub 

## About

This is an experiment to have free/cheaper activitypub instances running on AWS
(making use of free tiers as much as possible).

## Setup

Since ActivityPub events are push based, we will use [Lambda function URLs](https://docs.aws.amazon.com/lambda/latest/dg/lambda-urls.html) to handle the incoming events.

Since most of ActivityPub models are object based, we will use [DynamoDB](https://aws.amazon.com/dynamodb) 
for the storage of these objects.

Non-activity pub data can be stored in [S3](https://aws.amazon.com/s3) (usually images and media).

Using [CloudFront](https://aws.amazon.com/cloudfront), we can split up routing of a single domain to either the lambdas or the media paths
