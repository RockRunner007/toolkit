# Terraform Cheat Sheet

## Useful Links
- [Terraform CLI Commands](https://www.terraform.io/docs/commands/index.html)

## Common Commands

| Command                                                                 | Description                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| `terraform fmt` [docs](https://www.terraform.io/docs/commands/fmt.html) | Format Terraform configuration files                                                         |
| `terraform validate` [docs](https://www.terraform.io/docs/commands/validate.html) | Validate configuration files                                                                |
| `terraform plan` [docs](https://www.terraform.io/docs/commands/plan.html) | Create an execution plan                                                                    |
| `terraform apply` [docs](https://www.terraform.io/docs/commands/apply.html) | Apply changes to infrastructure                                                             |
| `terraform taint` [docs](https://www.terraform.io/docs/commands/taint.html) | Mark resource for recreation                                                                |
| `terraform import` [docs](https://www.terraform.io/docs/commands/import.html) | Import existing resources                                                                   |
| `terraform refresh` [docs](https://www.terraform.io/docs/commands/refresh.html) | Update state file with real infrastructure                                                  |
| `terraform graph` [docs](https://www.terraform.io/docs/commands/graph.html) | Generate visual representation of configuration or plan                                     |

## State Management

- List resources:  
	`terraform state list`
- Remove resource from state:  
	`terraform state rm 'packet_device.worker'`
- Remove resource (example):  
	`terraform state rm 'packet_device.<resource>'`

## Resource Operations

- Mark resource for recreation:  
	`terraform taint <resource>`
- Untaint resource:  
	`terraform untaint <resource>`
- Import resource:  
	`terraform import <resource> <id>`
	- Example:  
		`terraform import kubernetes_cluster_role_binding.aks dev01-cluster-admin`

## Plan and Destroy

- Create destroy plan:  
	`terraform plan -destroy -out aks.plan`
- Destroy specific target:  
	`terraform plan -destroy -target <resource>`

## Versions

- `terraform` (ensure correct version is installed)
