# cloudformation

AWS CloudFormation Templates

## vpc.yml

VPC CloudFormation stack with 2 availability zones, 2 public and 2 private subnets. The 2 private subnets are attached to 2 NAT gateways for 'inter-lambda' communication (ie. lambda.invoke). -- It is recommended that Security Groups control the inbound and outbound traffic rather than Network ACLs. This VPC is open to all traffic by default and will require the use of Security Groups bound to the VPC to 'lock it down'.

## peer.yml

VPC Peering CloudFormation stack with cross account peering. Use this stack to peer two VPCs across accounts.

## kms.yml

KMS CloudFormation stack initializes a hash token for encrypting data within the AWS environment.

## sqlserver.yml

RDS SQL Server CloudFormation stack creates an express instance of SQL Server with minimal capabilities.

## postgres.yml

RDS Postgres CloudFormation stack creates a minimal postgres instance in RDS.

## cognito.yml

Cognito CloudFormation stack initializes a Cognito User Pool and ID, for creating user management in mobile and web apps. See https://github.com/aws/aws-amplify/tree/master/packages/amazon-cognito-identity-js for getting started with the code.

## cloudtrail.yml

CloudTrail CloudFormation stack initializes an API usage and user activity tracking service.
