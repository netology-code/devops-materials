Чтобы воспользоваться зеркалом Terraform, сконфигурируйте terraform.   
В домашней директории создайте файл .terraformrc с  содержимым:

```
provider_installation {
  network_mirror {
    url = "https://registry.comcloud.xyz/"
  }
}
```

Теперь вы можете использовать network_mirror протокол для terraform.

Ниже пример использования, для aws провайдера:

```
terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
      version = "4.3.0"
    }
  }
```
