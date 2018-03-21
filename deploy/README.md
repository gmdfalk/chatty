# Microsoft Bot Service Azure Deployment
[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

## Preparation
### Configuration
Make sure to configure `azuredeploy.parameters.json` before deploying.

### Requirements
On OSX/Linux you also need to have node, npm, jq and azure-cli installed:

    brew update && brew install node azure-cli jq

### CLI-Setup
Run `az login` when first using the azure-cli.

## Deployment
The deployment scripts are taken from https://github.com/Azure/azure-quickstart-templates.
### PowerShell
    .\Deploy-AzureResourceGroup.ps1 -ResourceGroupLocation 'westeurope' -ArtifactStagingDirectory 'deploy' -ResourceGroupName 'dvagChatbotInnendienst' -Dev

### Bash
Validate the dev configuration:

    ./az-group-deploy.sh -a deploy -g dvagChatbotInnendienst -l westeurope -d -v
Deploy the dev config:

    ./az-group-deploy.sh -a deploy -g dvagChatbotInnendienst -l westeurope -d

