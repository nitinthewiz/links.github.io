---
title: "New – Access Resources in a VPC from Your Lambda Functions"
slug: new-access-resources-in-a-vpc-from-your-lambda-functions
date: 2016-02-11 21:25:32 -0600
category: 
external-url: https://aws.amazon.com/blogs/aws/new-access-resources-in-a-vpc-from-your-lambda-functions/
hash: 59ef0c094683ed1a8694988cc427cf19
year: 2016
month: 02
scheme: https
host: aws.amazon.com
path: /blogs/aws/new-access-resources-in-a-vpc-from-your-lambda-functions/

---

Your Lambda functions can now access Amazon Redshift data warehouses, Amazon ElastiCache clusters, Amazon Relational Database Service (RDS) instances, and service endpoints that are accessible only from within a particular VPC. In order to do this, you simply select one of your VPCs and identify the relevant subnets and security groups. Lambda uses this information to set up elastic network interfaces (ENIs) and private IP addresses (drawn from the subnet or subnets that you specified) so that your Lambda function has access to resources in the VPC.
