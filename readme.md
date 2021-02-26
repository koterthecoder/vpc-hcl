# Sample VPC using Terraform

## Basic Example

### set provider access and secret keys
```aws configure```

### initialize the tf configuration
```terraform init```

### plan the tf deployment
```terraform plan -out vpc.tfplan```

### apply the deployment
```terraform apply "vpc.tfplan"```


## Peering Example

This scenario is to be used with the repo `vpc-peer-hcl`

**Requestor:** `vpc-hcl`
**Acceptor:** `vpc-peer-hcl/security`

### Rename the peering configuration
```ren peering.tf.example peering.tf```

### Run tf plan
```terraform plan -var peer_role_arn="PEERING_ROLE_ARN" -var destination_vpc_id="SEC_VPC_ID" -out peer.tfplan```

### Apply the deployment
```terraform apply "peer.tfplan"```
