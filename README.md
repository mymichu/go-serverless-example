# Go-Serverless on AWS

This is an example of how to build a go serverless application with dynamodb, an API gateway in AWS. Therefore we use terraform to deploy the infrastructure to deploy the lambda functions.

## Deploy with Terraform

To deploy with terraform execute the following commands:
    
```bash
cd .infrastructure/stacks/development
terraform init
export AWS_SECRET_ACCESS_KEY=...
export AWS_ACCESS_KEY_ID=...
terraform plan
terraform apply
```

The AWS credentials are required to deploy the infrastructure. Can be found in AWS IAM.

to destroy the infrastructure execute the following command:

```bash
terraform destroy
```

# Go Build

To build the go application execute the following command:

```bash 
go build -o build/example cmd/main.go
```