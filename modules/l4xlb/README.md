# External TCP Proxy for Managed Instance Group Backend

<!-- BEGIN_TF_DOCS -->
## Providers

| Name | Version |
|------|---------|
| <a name="provider_google"></a> [google](#provider\_google) | >= 4.0.0 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [google_compute_backend_service.mig_backend](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_backend_service) | resource |
| [google_compute_global_forwarding_rule.forwarding_rule](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_global_forwarding_rule) | resource |
| [google_compute_health_check.mig_lb_hc](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_health_check) | resource |
| [google_compute_target_tcp_proxy.proxy](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_target_tcp_proxy) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_backend_migs"></a> [backend\_migs](#input\_backend\_migs) | List of MIGs to be used as backends. | `list(string)` | n/a | yes |
| <a name="input_external_ip"></a> [external\_ip](#input\_external\_ip) | External IP for the L7 XLB. | `string` | `null` | no |
| <a name="input_name"></a> [name](#input\_name) | External LB name. | `string` | n/a | yes |
| <a name="input_project_id"></a> [project\_id](#input\_project\_id) | Project id. | `string` | n/a | yes |

## Outputs

No outputs.
<!-- END_TF_DOCS -->