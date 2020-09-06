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