# Azure-ARM-Diagnostic-Policies

ARM documents to deploy diagnostic policies for specific resources

## Policies

### Initiative

![image](https://user-images.githubusercontent.com/8818198/92326806-257c2200-f055-11ea-8482-ae7638d343f6.png)

### Initiative - Policies

![image](https://user-images.githubusercontent.com/8818198/92326814-32007a80-f055-11ea-8412-64fc345f06f9.png)

### Policy Cosmos DB

![image](https://user-images.githubusercontent.com/8818198/92326826-3fb60000-f055-11ea-9491-1cc74aa673a1.png)

### Assign Policy Cosmos DB

![image](https://user-images.githubusercontent.com/8818198/92326840-58261a80-f055-11ea-9cf1-b8a6b8458953.png)

### Assign Policy Cosmos DB - Parameters

![image](https://user-images.githubusercontent.com/8818198/92326844-5fe5bf00-f055-11ea-8108-ea38d6240318.png)

## Diagnostic Setting - Cosmos DB

![image](https://user-images.githubusercontent.com/8818198/92326777-f5348380-f054-11ea-82fd-9e02d62e7da9.png)

![image](https://user-images.githubusercontent.com/8818198/92326764-dcc46900-f054-11ea-9373-2f13bfb14b70.png)

## Deployment

### Azure CLI

```azurecli-interactive
az deployment sub create  --location westeurope --template-file .\Policy.json --parameters "@Policy.parameters.json"
```

### Powershell

```powershell
New-AzDeployment -Name "diagPolicies" -location "West Europe" -TemplateFile .\Policy.json  -verbose -TemplateParameterFile .\Policy.parameters.json
```

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FMarkusMeyer13%2FAzure-ARM-Diagnostic-Policies%2Fmaster%2FPolicy.json)  [![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2raw.githubusercontent.com%2FMarkusMeyer13%2FAzure-ARM-Diagnostic-Policies%2Fmaster%2FPolicy.json)
