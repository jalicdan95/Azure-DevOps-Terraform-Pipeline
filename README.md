<h1><strong>Azure DevOps Terraform Demo</strong></h1>
<p><span style="text-decoration: underline;"><strong>PART 1: Terraform Configurations</strong></span></p>
<p><span style="font-weight: 400;">This part documents the Terraform configuration files (main.tf, backend.tf, provider.tf, variables.tf) written to successfully deploy Azure resources: Network interface, resource group, subnet, virtual machine, and virtual network. Ultimately, publish our repo and we destroy our infrastructure.</span></p>
<p><span style="font-weight: 400;">Note: We created a remote backend using Azure storage to migrate from local state to remote.</span></p>
<p>&nbsp;</p>
<p><span style="text-decoration: underline;"><span style="font-weight: 400;"><strong>PART 2: Azure DevOps Pipeline</strong></span></span></p>
<p><span style="font-weight: 400;">This part demonstrates the capabilities within Azure DevOps (ADO) pipelines. Essentially, we are importing our repo from part 1 into ADO and creating a CI pipeline with terraform commands. We then release what we build in a CD pipeline and the end result will be the same as part 1: a remote backend and our 5 Azure resources created. The pipeline will also destroy our infrastructure once approved.</span></p>
