# Azure DevOps pipeline decorators

This repository contains a set of sample decorators for Azure DevOps pipelines.

Refer to the [Azure DevOps Pipeline Decorators v1.pdf](./Azure%20DevOps%20Pipeline%20Decorators%20v1.pdf) document for more information on pipeline decorators and the necessary infrastructure to use them.

Refer to the [.pipelines/publish-extension.yml](./.pipelines/publish-extension.yml) file for an example of how to use an Azure Pipeline to automate publishing the sample pipeline decorator extension to the Visual Studio Marketplace.

The YAML pipeline to build and publish this extension references a variable group named 'pipeline-decorators-variables' that contains the following variables:

- `PersonalAccessToken`: A personal access token with access to publish extensions to the Visual Studio Marketplace. See https://learn.microsoft.com/azure/devops/extend/publish/command-line for more information. You should change this variable's type to 'secret' to hide its value. This variable is mandatory and the pipeline will fail if it is not defined.
- `ShareWithOrgs`: A space-separated list of Azure DevOps organizations to share the extension with. This variable is optional and the pipeline will not fail if it is not defined.
