# terraform-iacdevops-with-aws-codepipeline
terraform-iacdevops-with-aws-codepipeline

Processes/Creations

Using Terraform, I managed my terraform configuration files and stored them into a GitHub repository. 
Created a AWS CodePipline and referenced the source as my Github Repository.
Created a AWS CodeBuild project for dev environment deploy stage and leveraged the AWS CodeBuild tool to deploy terraform configurations in AWS.
Created a manual approval stage in the pipeline.
Created a CodeBuild project for the staging environment deploy 

The Dev environment is composed of…
- Creation of a DNS record
- Application Load Balancer
- Certificate Manager for creating SSL certificates
- Auto Scaling groups with launch templates
- NAT gateway for VPC and outbound communication
- IAM Roles
- Batch Instances
- SNS for Auto Scaling group alerts.

Once the Dev Deploy Stage is successful it would move to the Manual approval stage.
Using SNS, an email will be sent to the respective manager for approval.
Once approved, the process will move towards the Stag Deploy Stage.

<img width="1065" alt="Screenshot 2023-01-11 at 3 12 29 PM" src="https://user-images.githubusercontent.com/101589213/211919812-7ddb44d9-5727-44d3-8335-02528d23399c.png">
<img width="1080" alt="Screenshot 2023-01-11 at 3 12 19 PM" src="https://user-images.githubusercontent.com/101589213/211919825-82663590-4387-458c-9339-8b40952e3c75.png">
<img width="1082" alt="Screenshot 2023-01-11 at 3 12 07 PM" src="https://user-images.githubusercontent.com/101589213/211919840-c283be8e-f25d-4fc8-94ad-74c8a27461ae.png">
