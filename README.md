# Web App with diagnostics logging to Storage Account Blob Container. Deploy resources into a different resource groups using nested  template.

This template deploys a Web App with diagnostics logging to Storage Account Blob Container. It deploys the storage account into a different resource group than the WebApps and the App Service Plan. It uses nested template. It also enables FREB and Detailed Error logs.

This template uses the `listAccountSas` function to retrieve Storage Account SAS and then connect Storage Account (and its blob container) with Web App ([ARM function reference](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-template-functions-resource#listaccountsas-listkeys-listsecrets-and-list), [API endpoint reference](https://docs.microsoft.com/en-us/rest/api/storagerp/storageaccounts/listaccountsas)). By using `listAccountSas` whole solution can be deployed in a single step - there is no need for getting and providing Storage Account SAS explicitly by the user.

`Tags: App Service, Web Application, Storage Account, Diagnostics Logs, Blob Container, Nested ARM template, Linked Template, Different Resource Group`
