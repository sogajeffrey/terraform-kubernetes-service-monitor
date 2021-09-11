# terraform-kubernetes-service-monitor
Kubernetes Prometheus Service Monitor

## Providers

| Name | Version |
|------|---------|
| <a name="provider_kubernetes"></a> [kubernetes](#provider\_kubernetes) | n/a |

## Resources

| Name | Type |
|------|------|
| [kubernetes_manifest.service_monitor](https://registry.terraform.io/providers/hashicorp/kubernetes/latest/docs/resources/manifest) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_label_key"></a> [label\_key](#input\_label\_key) | n/a | `string` | n/a | yes |
| <a name="input_label_value"></a> [label\_value](#input\_label\_value) | n/a | `string` | n/a | yes |
| <a name="input_name"></a> [name](#input\_name) | n/a | `string` | n/a | yes |
| <a name="input_namespace"></a> [namespace](#input\_namespace) | n/a | `string` | n/a | yes |
| <a name="input_namespace_selector"></a> [namespace\_selector](#input\_namespace\_selector) | n/a | `string` | n/a | yes |
| <a name="input_port"></a> [port](#input\_port) | n/a | `string` | n/a | yes |

## Example

```
module "test_service_monitor" {
  source = "./modules/service-monitor"
  name = "test-sm"
  namespace = "dev"
  port = "service-port"
  namespace_selector = "namespace"
  label_key = "app"
  label_value = "test"
}
```