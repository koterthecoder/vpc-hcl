# Sample VPC using Terraform


### set provider access and secret keys
```aws configure```

### initialize the tf configuration
```terraform init```

### plan the tf deployment
```terraform plan -out vpc.tfplan```

### apply the deployment
```terraform apply "vpc.tfplan"```