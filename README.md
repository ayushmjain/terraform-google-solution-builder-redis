# terraform-google-solution-builder-redis

## Description
### Tagline
Memorystore for Redis provides a fully-managed service that is powered by the Redis in-memory data store to build application caches.

### Detailed
This composition unit creates a managed redis instance of the version Redis 6.x with a memory size of 1GB.

The resources/services/activations/deletions that this module will create/trigger are:

- Create a redis instance with the provided name.

### PreDeploy
To deploy this blueprint you must have an active billing account and billing permissions.

## Documentation
- [Redis](https://cloud.google.com/memorystore/docs/redis/memorystore-for-redis-overview)

## Cost
[Blueprint cost details](https://cloud.google.com/products/calculator/#id=91f31d97-8470-4b79-a28e-2583b2be3f26)

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
| module\_dependency | n/a |
| redis\_host | n/a |
| redis\_port | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Requirements

These sections describe requirements for using this module.

### Software

The following dependencies must be available:

- [Terraform][terraform] v0.13
- [Terraform Provider for GCP][terraform-provider-gcp] plugin v3.0

### Service Account

A service account with the following roles must be used to provision
the resources of this module:

- Redis Admin: `roles/redis.admin`

The [Project Factory module][project-factory-module] and the
[IAM module][iam-module] may be used in combination to provision a
service account with the necessary roles applied.

### APIs

A project with the following APIs enabled must be used to host the
resources of this module:

- Google Cloud Memorystore for Redis API: `redis.googleapis.com`

The [Project Factory module][project-factory-module] can be used to
provision a project with the necessary APIs enabled.

## Contributing

Refer to the [contribution guidelines](./CONTRIBUTING.md) for
information on contributing to this module.

[iam-module]: https://registry.terraform.io/modules/terraform-google-modules/iam/google
[project-factory-module]: https://registry.terraform.io/modules/terraform-google-modules/project-factory/google
[terraform-provider-gcp]: https://www.terraform.io/docs/providers/google/index.html
[terraform]: https://www.terraform.io/downloads.html

## Security Disclosures

Please see our [security disclosure process](./SECURITY.md).
