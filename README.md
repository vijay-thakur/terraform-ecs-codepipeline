# demo-cicd-codepipeline

## Terraform Create ECS with CodePipeline

You can change variables in `variables.tfvars` , 

For example: I want to create a VPC with CIDR ( 10.92.0.0/16 ), two public subnet and two private subnet.

```
vpc_cidr = "10.92.0.0/16"
environment = "production"
public_subnet_cidrs = ["10.92.0.0/24", "10.92.1.0/24"]
private_subnet_cidrs = ["10.92.50.0/24", "10.92.51.0/24"]
availibility_zones = ["us-west-2a", "us-west-2b"]
region = "us-west-2"
ami_image = "ami-09568291a9d6c804c"
ecs_key = "demo"
instance_type = "t2.medium"
repo_owner = "vijay-thakur"
repo_name = "demo-cicd-codepipeline"
github_oauth_token = "github_oauth_token"

```

Then run

```
terraform init
terraform plan -var-file=variables.tfvars
terraform apply -var-file=variables.tfvars
```
