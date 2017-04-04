# DevOpsAssessment

## Objective:
Use CM tools such as Puppet, Ansible, or Chef to automate the installation of basic Drupal or WordPress. Setup a sample site. Automate the solution using Cloudformation template.

I have gone through various sample templates that are available in online. Previously I worked on creating resources like VPC, subnet, Internet gateway, EC2instance with user data and S3 buckets. But this task seems to be a bit different. Here we used CloudFormation::init to create configuration files for installing packages. 

After going through the following sample which is available online https://s3.amazonaws.com/cloudformation-examples/IntegratingAWSCloudFormationWithOpscodeChef.pdf I thought its something easy to implement. But after looking at my IAM policy I realized that I am restricted to ELB, AutoScaling Groups and RDS. So I thought this should be implemented with by installing the database itself on the EC2 instance. I tried to modify the template accordingly.

Step1:
I referred the videos availabe and came to a conclusion on what all resources required to host wordpress CMS in the cloud.

Step2: 
I started working on the template accordingly and finally came up with one CFT.

Step3:
After uploading the JSON file in the Cloud Formation Section I encountered many formatting issues.

Step4:
So I planned to validate it using JSON validator. Here I got rid of few problems.

Step5:
Even after validating using JSON validator I came across few more errors like unsupported property group name and tags must be of type list. By going through developer forums I realized where I got wrong.

Step6:
After resolving these errors I finally done with my stack creation.

Step7:
As per my understanding I represented the flow of events in the architecture diagram.
