
### CLI-driven runs (Terraform & OpenTofu)

1. Add a configuration block to your IaC files to set up the cloud integration. For Terraform users this is typically placed in a `.tf` file. For OpenTofu users, use the equivalent OpenTofu configuration idiom.

Example (Terraform HCL):

```hcl
terraform { 
  cloud { 
    organization = "<<your-org>>" 
    workspaces { 
      name = "<<your-workspace>>" 
    } 
  } 
}
```

2. Run `terraform init` (Terraform) or the equivalent OpenTofu initialization command to initialize the workspace.
3. Run `terraform apply` (Terraform) or the equivalent OpenTofu apply/run command to start the first run for this workspace.

For more details on Terraform CLI-driven runs, see: https://developer.hashicorp.com/terraform/cloud-docs/run/cli. OpenTofu users should consult OpenTofu documentation for equivalent CLI workflows.
