<h1><strong>Azure DevOps Terraform Demo</strong></h1>
<p><span style="text-decoration: underline;"><strong>PART 1: Terraform Configurations</strong></span></p>
<p><span style="font-weight: 400;">This part documents the Terraform configuration files (main.tf, backend.tf, provider.tf, variables.tf) written to successfully deploy Azure resources: Network interface, resource group, subnet, virtual machine, and virtual network. Ultimately, publish our repo and we destroy our infrastructure.</span></p>
<p><span style="font-weight: 400;">Note: We created a remote backend using Azure storage to migrate from local state to remote.</span></p>
<p>&nbsp;</p>
<p><span style="text-decoration: underline;"><span style="font-weight: 400;"><strong>PART 2: Azure DevOps Pipeline</strong></span></span></p>
<p><span style="font-weight: 400;">This part demonstrates the capabilities within Azure DevOps (ADO) pipelines. Essentially, we are importing our repo from part 1 into ADO and creating a CI pipeline with terraform commands: init, validate, fmt, plan. Additionally, we integrate Archive files and PublishBuildArtifacts tasks. </span></p>
<p><span style="font-weight: 400;">We then build a release CD pipeline that includes the tasks: extract files, install terraform latest, terraform init, and terraform apply. Our 5 resources will be created as demonstrated in part 1. </span></p>
<p><span style="font-weight: 400;">Additionally, we clone the deployment, rename it as "Destroy", and update the terraform apply command to terraform destroy. We trigger this for pre-approval and once approved our infrastructure is wiped clean.&nbsp;</span></p>

![image](https://github.com/user-attachments/assets/ef4f702c-2941-4843-9f4a-ca5e2eea786d)
