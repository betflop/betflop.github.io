# Terraform 

### Знакомство с Terraform

- Инструмент для декларативного описания инфраструктуры
- Описание инфраструктуры хранится в конфигурационных .tf-файлах
- State

```hcl
terraform -h

terraform init
terraform plan
terraform apply
terraform destroy
terraform show
```

```terraform
provider "name" {
    key = value
}

resource "type" "name" {
    key = value
}

variable "name" {
    type = ""
    default = ""
}
```
