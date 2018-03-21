# Microsoft Bot Service Azure Deployment
[![Deploy to Azure][Deploy Button]][Deploy deploy]

[Deploy Button]: https://azuredeploy.net/deploybutton.png
[Deploy deploy]: https://azuredeploy.net

## Preparation
### Configuration
Make sure to configure `azuredeploy.parameters.json` before deploying.

### Requirements
On OSX/Linux you also need to have node, npm, jq and azure-cli installed:

    brew update && brew install node azure-cli jq

### CLI-Setup
Run `az login` when first using the azure-cli.

## Deployment (to Dev)
The deployment scripts are taken from https://github.com/Azure/azure-quickstart-templates.
### PowerShell
    .\Deploy-AzureResourceGroup.ps1 -ResourceGroupLocation 'westeurope' -ArtifactStagingDirectory 'deploy' -ResourceGroupName 'dvag-chatbot-innendienst' -Dev

### Bash
    ./az-group-deploy.sh -a deploy -g dvag-chatbot-innendienst -l westeurope -d

