# Voice Powered Analytics 

In this workshop, you will build an Alexa skill that queries metrics from a data lake, which you will define. The goal after leaving this workshop, is for you to understand how to uncover Key Performance Indicators (KPIs) from a data set, build and automate queries for measuring those KPIs, and access them via Alexa voice-enabled devices. Startups can make available voice powered analytics to query at any time, and Enterprises can deliver these types of solutions to stakeholders so they can have easy access to the Business KPIs that are top of mind.

This workshop requires fundamental knowledge of AWS services, but is designed for first time users of Athena, Alexa, and Lambda. We have broken the workshop into two sections or focus topics. These are:

- Querying data in a data lake using Athena (based on objects in S3) to generate answers for Alexa
- Building a custom Alexa skill to access the analytics queries from Athena

We expect most attendees to be able to complete the full workshop in **2 hours**.



## Prerequisites

Please make sure you have the following available prior to the workshop.

- [Amazon Developer](https://developer.amazon.com/alexa) account (Free) **Note** This is different from a typical AWS workflow.



## Lab Setup

We have provided a CloudFormation template to create baseline resources needed by this lab but are not the focus of the workshop. These include IAM Roles, IAM Policies, a DynamoDB table, and a CloudWatch Event rule. These are listed as outputs in the CloudFormation template in case you want to inspect them.

**Please launch the template below so that the resources created will be ready by the time you get to those sections in the lab guides.**

**Pick the desired region that's closest to your location for optimal performance **



Each attendee will deploy their own CloudFormation stack (user_template.yml). They will need the name of the stack that was create from the base.yml in order to import certain values. 



1. Login to the AWS Management Console. 

2. Navigate to Services and then to CloudFormation. 

3. Select Create stack. 

4. Choose <strong>Upload a template file</strong>.  

5. Upload file <strong> user_template.yml </strong>. 

6. Click <strong>Next</strong>.

7. Enter the following values for your parameters.

Input Name | Value 
:---: | :---:
Stack name | VPA-<your_alias> (e.g. VPA-alexe)
BaseStackName | <Your_Company>VPA (e.g. AmazonVPA)
DDBReadCapacityUnits | 5
DDBWriteCapacityUnits | 5 


8. Accept all defaults and acknolwedge that IAM resources will be created and then click <strong>Create stack</strong>. 

9. Once the stack is created, move on to the Athena Lab. 

When you launch the template you will be asked for a few inputs. Use the following table for reference.

<details>
<summary><strong>Watch a video of launching CloudFormation (Click to expand)</strong></summary><p>

![launcg CloudFormation](./media/images/vpa-cloudformation-launch.gif)

</details>

<table><tr><td>Region</td> <td>Launch Template</td></tr>
<tr><td>US-EAST-1</td> <td><a href="https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new" target="_blank"><IMG SRC="./media/images/CFN_Image_01.png"></a></td></tr></table>

#### Main Modules: 
1. [Amazon Athena Section](1-Voice-Powered-Analytics-Athena-Lab.md)
1. [Amazon Alexa Section](2-Voice-Powered-Analytics-Alexa-Skills-Lab.md)