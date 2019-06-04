This guide is used when running the VPA workshop with multiple users out of a single account. This makes it easy for administrators to create resources on behalf of users and streamline the overall approach. 



Admin - the admin will deploy a CloudFormation template that will create IAM roles and policies for this workshop. 

Go to CloudFormation in us-east-1 and deploy the template base.yml with the name of QualcommVPA. 





Users 


Each attendee will deploy their own CloudFormation stack (user_template.yml). They will need the name of the stack that was create from the base.yml in order to import certain values. 



1. Login to the AWS Management Console. 

2. Navigate to Services and then to CloudFormation. 

3. Select Create stack. 

4. Choose <strong>Upload a template file</strong>.  

5. Upload file <strong> user_template.yml </strong>. 

6. Click <strong>Next</strong>.

7. For Stack name enter VPA-<your-alias> (e.g. VPA-alexe).

8.  For BaseStackName, enter QualcommVPA. 

9. Accept all defaults and acknolwedge that IAM resources will be created and then click <strong>Create stack</strong>. 

10. Once the stack is created, move on to the Athena Lab. 

    