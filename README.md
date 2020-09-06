# Azure-ARM-Diagnostic-Policies
ARM documents to deploy diagnostic policies for specific resources

## Deployment

### Azure CLI

```azurecli-interactive
az deployment sub create --location westeurope --template-file .\Policy.json --parameters '{ \"profileName\": { \"value\": \"MarkusMeyer-setbypolicy_logAnalytics\" }, \"logAnalytics\": { \"value\": \"DefaultWorkspace-e687f850-b05f-4061-8ccc-e950cca41423-WEU\" }, \"metricsEnabled\": { \"value\": \"True\" }, \"logsEnabled\": { \"value\": \"True\" }, \"effect\": { \"value\": \"DeployIfNotExists\" } }'
```

### Powershell

```powershell
New-AzDeployment -Name "diagPolicies" -location "West Europe" -TemplateFile .\Policy.json  -verbose -TemplateParameterFile .\Policy.parameters.json
```

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FMarkusMeyer13%2FAzure-ARM-Diagnostic-Policies%2Fmaster%2FPolicy.json)  [![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2raw.githubusercontent.com%2FMarkusMeyer13%2FAzure-ARM-Diagnostic-Policies%2Fmaster%2FPolicy.json)
