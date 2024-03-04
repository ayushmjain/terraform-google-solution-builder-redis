# Simple Example

This example illustrates how to use the `solution-builder-redis` module.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| network\_name | VPC network name where the Redis instance is created | `string` | `null` | no |
| project\_id | GCP project ID where the Redis instance is created | `string` | n/a | yes |
| redis\_instance\_name | Redis instance name | `string` | n/a | yes |
| region | GCP region where the Redis instance is created | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| redis\_host | n/a |
| redis\_port | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

To provision this example, run the following from within this directory:
- `terraform init` to get the plugins
- `terraform plan` to see the infrastructure plan
- `terraform apply` to apply the infrastructure build
- `terraform destroy` to destroy the built infrastructure
