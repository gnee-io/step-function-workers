# Dynamic parallelism using AWS Step Functions

This repo contains an example of a simple fork join process using lambda and step functions.

![flow](stepfunctions_graph.png?raw=true "Step function workflow")

## Run the examples

This assumes you are using the default AWS profile.

### Terraform

Enter the tf directory and run terraform plan/apply, e.g.

```sh
cd tf
terraform init
terraform plan
terraform apply
```

### Deploy lambdas

Edit the `artifacts_s3_bucket_name` variable in the `scripts/deploy.sh` file to refer to a bucket you own.

```sh
make build && make deploy
```