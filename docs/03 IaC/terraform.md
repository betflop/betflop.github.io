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
!!! note

    Провайдер это уже кем то написанная программа которая позволяет вам на языке
    Терраформа общаться с какой то системой где вы будете делать свою инфраструктуру

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

### Пример работы с докером

=== ":octicons-file-code-16: `container.tf`"

    ```terraform
    variable "external_port" { 
        type = number
        default = "8080"
    }

    resource "docker_image" "nginx-image" {
        name = "nginx:latest"
    }

    resource "docker_container" "nginx-container" {
        name = "nginx"
        image = docker_image.nginx-image.image_id
        ports {
            internal = 80
            external = var.external_port
        }
    }
    ```

=== ":octicons-file-code-16: `docker.tf`"

    ```terraform
    terraform {
        required_providers {
            docker = {
                source = "kreuzwerker/docker"
                    version = "2.24.0"
            }
        }
    }
    ```


