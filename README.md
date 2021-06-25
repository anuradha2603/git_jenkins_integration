## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.15.1 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_gke-ws"></a> [gke-ws](#module\_gke-ws) | git@github.com:acxiomanalyticsgcp/acoe-google-gke-t.git | n/a |

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_default_max_pods_per_node"></a> [default\_max\_pods\_per\_node](#input\_default\_max\_pods\_per\_node) | The default maximum number of pods per node. | `number` | n/a | yes |
| <a name="input_enable_binary_authorization"></a> [enable\_binary\_authorization](#input\_enable\_binary\_authorization) | n/a | `bool` | n/a | yes |
| <a name="input_enable_private_nodes"></a> [enable\_private\_nodes](#input\_enable\_private\_nodes) | n/a | `bool` | n/a | yes |
| <a name="input_enable_vertical_pod_autoscaling"></a> [enable\_vertical\_pod\_autoscaling](#input\_enable\_vertical\_pod\_autoscaling) | n/a | `bool` | n/a | yes |
| <a name="input_horizontal_pod_autoscaling"></a> [horizontal\_pod\_autoscaling](#input\_horizontal\_pod\_autoscaling) | Enable horizontal pod autoscaling addon | `bool` | n/a | yes |
| <a name="input_http_load_balancing"></a> [http\_load\_balancing](#input\_http\_load\_balancing) | Enable httpload balancer addon | `bool` | n/a | yes |
| <a name="input_ip_range_pods_cidr"></a> [ip\_range\_pods\_cidr](#input\_ip\_range\_pods\_cidr) | n/a | `string` | n/a | yes |
| <a name="input_ip_range_services_cidr"></a> [ip\_range\_services\_cidr](#input\_ip\_range\_services\_cidr) | n/a | `string` | n/a | yes |
| <a name="input_master_ipv4_cidr_block"></a> [master\_ipv4\_cidr\_block](#input\_master\_ipv4\_cidr\_block) | CIDR block to be used for the GKE master | `string` | n/a | yes |
| <a name="input_network"></a> [network](#input\_network) | The VPC network to host the cluster in | `any` | n/a | yes |
| <a name="input_network_policy"></a> [network\_policy](#input\_network\_policy) | Enable network policy addon | `bool` | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | The region to host the cluster in | `any` | n/a | yes |
| <a name="input_remove_default_node_pool"></a> [remove\_default\_node\_pool](#input\_remove\_default\_node\_pool) | n/a | `bool` | n/a | yes |
| <a name="input_subnet_ip"></a> [subnet\_ip](#input\_subnet\_ip) | n/a | `string` | n/a | yes |
| <a name="input_subnets"></a> [subnets](#input\_subnets) | The list of subnets being created | `list(map(string))` | n/a | yes |
| <a name="input_auto_repair"></a> [auto\_repair](#input\_auto\_repair) | Whether Auto repair nodes will be true or false | `bool` | `true` | no |
| <a name="input_auto_upgrade"></a> [auto\_upgrade](#input\_auto\_upgrade) | Whether Auto upgrade nodes will be true or false | `bool` | `true` | no |
| <a name="input_client_name"></a> [client\_name](#input\_client\_name) | n/a | `string` | `""` | no |
| <a name="input_disk_size_gb"></a> [disk\_size\_gb](#input\_disk\_size\_gb) | Size of the disk attached to each node, specified in GB. | `number` | `100` | no |
| <a name="input_disk_type"></a> [disk\_type](#input\_disk\_type) | Type of the disk attached to each node | `string` | `"pd-standard"` | no |
| <a name="input_env"></a> [env](#input\_env) | n/a | `string` | `""` | no |
| <a name="input_image_type"></a> [image\_type](#input\_image\_type) | The image type to use for this node. | `string` | `"COS"` | no |
| <a name="input_ip_range_pods"></a> [ip\_range\_pods](#input\_ip\_range\_pods) | The _name_ of the secondary subnet ip range to use for pods | `string` | `"pii-mavenwave-gke-pods"` | no |
| <a name="input_ip_range_services"></a> [ip\_range\_services](#input\_ip\_range\_services) | The _name_ of the secondary subnet range to use for services | `string` | `"pii-mavenwave-gke-services"` | no |
| <a name="input_local_ssd_count"></a> [local\_ssd\_count](#input\_local\_ssd\_count) | Number of local SSDs to use to back ephemeral storage. | `number` | `0` | no |
| <a name="input_machine_type"></a> [machine\_type](#input\_machine\_type) | The name of a Google Compute Engine machine type | `string` | `"e2-medium"` | no |
| <a name="input_max_count"></a> [max\_count](#input\_max\_count) | node pool maximum count | `number` | `2` | no |
| <a name="input_min_count"></a> [min\_count](#input\_min\_count) | node pool minimum count | `number` | `1` | no |
| <a name="input_name"></a> [name](#input\_name) | The name of the cluster | `string` | `"pii-mavenwave-k8s-cluster"` | no |
| <a name="input_node_locations"></a> [node\_locations](#input\_node\_locations) | The list of zones in which the cluster's nodes are located | `string` | `"us-central1-b, us-central1-c"` | no |
| <a name="input_node_pool_name"></a> [node\_pool\_name](#input\_node\_pool\_name) | The name of the node pool | `string` | `"default-node-pool"` | no |
| <a name="input_preemptible"></a> [preemptible](#input\_preemptible) | A boolean that represents whether or not the underlying node VMs are preemptible | `bool` | `false` | no |
| <a name="input_project_id"></a> [project\_id](#input\_project\_id) | The project ID to host the cluster in (required) | `string` | `""` | no |
| <a name="input_project_number"></a> [project\_number](#input\_project\_number) | The project number to host the cluster in (required) | `string` | `""` | no |
| <a name="input_shared_vpc_host"></a> [shared\_vpc\_host](#input\_shared\_vpc\_host) | Makes this project a Shared VPC host if 'true' (default 'false') | `bool` | `false` | no |
| <a name="input_subnetwork"></a> [subnetwork](#input\_subnetwork) | The subnetwork to host the cluster in | `string` | `""` | no |
| <a name="input_vpc_name"></a> [vpc\_name](#input\_vpc\_name) | n/a | `string` | `""` | no |
| <a name="input_vpc_project"></a> [vpc\_project](#input\_vpc\_project) | The project ID to host the network | `string` | `""` | no |
| <a name="input_zones"></a> [zones](#input\_zones) | The zones to host the cluster in | `list(string)` | <pre>[<br>  "us-central1-a",<br>  "us-central1-b",<br>  "us-central1-f"<br>]</pre> | no |

## Outputs

No outputs.
