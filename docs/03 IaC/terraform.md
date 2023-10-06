# Terraform 

### Знакомство с Terraform

- Инструмент для декларативного описания инфраструктуры
- Описание инфраструктуры хранится в конфигурационных .tf-файлах
- State

```terraform
terraform -h

terraform init
terraform plan
terraform apply
terraform destroy
terraform show
```

- Провайдер это уже кем то написанная программа которая позволяет вам на языке
Терраформа общаться с какой то системой где вы будете делат свою инфраструктуру

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
