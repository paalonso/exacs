# RUNTIME

## Running with OCI Resource Manager Service

**DEPLOY WITH ORM** </br></br>[<img src="content/DeployToOCI.svg"  height="30" align="center">](https://cloud.oracle.com/resourcemanager/stacks/create?zipUrl=https://github.com/oci-landing-zones/terraform-oci-modules-orchestrator/archive/refs/tags/v2.0.6.zip&zipUrlVariables={"configuration_source":"github","github_token":"","github_configuration_repo":"paalonso/exacs","github_configuration_branch":"master","github_configuration_files":"oci_open_lz_one-oe_iam.auto.tfvars.json,oci_open_lz_hub_a_network_light.auto.tfvars.json"})  </br></br> And follow these steps:</br>1. Accept terms,  wait for the configuration to load. </br>2. Set the working directory to “rms-facade”. </br>3. Set the stack name you prefer.</br>4. Set the terraform version to 1.5.x. Click Next. </br>5. Accept the default files. Click Next. Optionally, replace with your json/yaml config files. </br>6. Un-check run apply. Click Create. </br> </br>

## Running with Terraform CLI

### Get the OCI LZ Orchestrator

#### Clone the Orchestrator:

```
git clone git@github.com:oci-landing-zones/terraform-oci-modules-orchestrator.git
```

#### Initialize the Orchestrator:

```
terraform init
```

### One Single Stack

```
$ terraform plan -var-file ../exacc/1stack/oci-credentials.tfvars.json \
-var-file ../exacs/1stack/oci_open_lz_one-oe_iam.auto.tfvars.json \
-var-file ../exacs/1stack/oci_open_lz_hub_a_network_light.auto.tfvars.json \
-state ../exacs/1stack/terraform.tfstate
```

*** NOTE: Rest of the configuration files are Work In Progress***