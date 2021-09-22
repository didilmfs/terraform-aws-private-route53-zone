# terraform-aws-private-route53-zone


[![Terraform Version](https://img.shields.io/badge/Terraform%20Version->=0.13.0,<=0.13.7-blue.svg)](https://releases.hashicorp.com/terraform/)
[![Release](https://img.shields.io/github/release/traveloka/terraform-aws-private-route53-zone.svg)](https://github.com/traveloka/terraform-aws-private-route53-zone/releases)
[![Last Commit](https://img.shields.io/github/last-commit/traveloka/terraform-aws-private-route53-zone.svg)](https://github.com/traveloka/terraform-aws-private-route53-zone/commits/master)
[![Issues](https://img.shields.io/github/issues/traveloka/terraform-aws-private-route53-zone.svg)](https://github.com/traveloka/terraform-aws-private-route53-zone/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/traveloka/terraform-aws-private-route53-zone.svg)](https://github.com/traveloka/terraform-aws-private-route53-zone/pulls)
[![License](https://img.shields.io/github/license/traveloka/terraform-aws-private-route53-zone.svg)](https://github.com/traveloka/terraform-aws-private-route53-zone/blob/master/LICENSE)
![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)

## Description

Terraform module to create a private Route53 hosted zone

## Table of Content

- [Description](#Description)
- [Table of Content](#table-of-content)
- [Prerequisites](#Prerequisites)
- [Dependencies](#Dependencies)
- [Terraform Versions](#Terraform%20Versions)
- [Terraform Providers](#Terraform%20Providers)
- [Getting Started](#Getting_Started)
- [Inputs](#Inputs)
- [Outputs](#Outputs)
- [Contributing](#Contributing)
- [Author](#Author)
- [License](#License)

## Prerequisites

In order to provision this module, it is require some information from an existing resources as input parameter, those resources are:

- AWS VPC, input variable that require the information from this resource are, `main_vpc`, and `secondary_vpcs` 

## Dependencies

Doesn't have any dependencies to any other Terraform module

## Terraform Versions

This module was created on 04/04/2018 using Terraform version 0.11.14. The latest stable version of Terraform which this module tested working is Terraform 0.13.7 on 20/09/2021

## Terraform Providers

| Name | Version |
| ---- | ------- |
| aws  | ~> 2.49 |

## Getting Started

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.13 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_route53_zone.main](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/route53_zone) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_additional_vpc_ids"></a> [additional\_vpc\_ids](#input\_additional\_vpc\_ids) | List of additional VPC ID's that will be associated with this hosted zone | `list(map(string))` | `[]` | no |
| <a name="input_default_vpc_region"></a> [default\_vpc\_region](#input\_default\_vpc\_region) | Default region of lists of the associated VPC's. | `string` | n/a | yes |
| <a name="input_environment"></a> [environment](#input\_environment) | Environment this Route 53 zone belongs to | `string` | n/a | yes |
| <a name="input_force_destroy"></a> [force\_destroy](#input\_force\_destroy) | Whether to destroy all records inside if the hosted zone is deleted | `bool` | `false` | no |
| <a name="input_main_vpc"></a> [main\_vpc](#input\_main\_vpc) | Main VPC ID that will be associated with this hosted zone | `string` | n/a | yes |
| <a name="input_name"></a> [name](#input\_name) | Name of the hosted zone | `string` | n/a | yes |
| <a name="input_product_domain"></a> [product\_domain](#input\_product\_domain) | Abbreviation of the product domain this Route 53 zone belongs to | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_zone_id"></a> [zone\_id](#output\_zone\_id) | The hosted zone id |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Contributing

This module accepting or open for any contributions from anyone, please see the [CONTRIBUTING.md](https://github.com/traveloka/terraform-aws-private-route53-zone/blob/master/CONTRIBUTING.md) for more detail about how to contribute to this module.

## Authors

* [Abi](https://github.com/abihf)

## License

This module is under Apache License 2.0 - see the [LICENSE](https://github.com/traveloka/terraform-aws-private-route53-zone/blob/master/LICENSE) file for details.
