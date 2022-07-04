# Sample Nginx web server deployed via Docker provider

## Usage:
1. Initialize the workspace:
```shell
terraform init
```
2. Output deployment plan:
```shell
terraform plan
```
3. Deploy the application:
```shell
terraform apply
```
4. To check the running container use:
```shell
docker ps
```
5. To access sample nginx webpage go to [http://localhost:8080/](http://localhost:8080/)
6. To destroy the app use:
```shell
terraform destroy
```

## Notes:
1. `keep_locally` (Boolean) If true, then the Docker image won't be deleted on destroy operation. If this is false, it will delete the image from the docker local storage on destroy operation. [Link](https://registry.terraform.io/providers/kreuzwerker/docker/latest/docs/resources/image)
2. `latest` (String, Deprecated) The ID of the image in the form of `sha256:<hash>` image digest. Do not confuse it with the default latest tag. [Link](https://registry.terraform.io/providers/kreuzwerker/docker/latest/docs/resources/image)

## Reference:
[Docker provider](https://registry.terraform.io/providers/kreuzwerker/docker/latest/docs)