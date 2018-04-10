# Delopying an Application to Azure

Demo for deploying a test web app to Azure.

## Starting the Application

To run locally use:

`npm start`

Currently the node application will run on https://localhost:1000

#### Zip the app with Bash
`zip -r myAppFiles.zip .`
#### Zip the app with PowerShell
`Compress-Archive -Path * -DestinationPath myAppFiles.zip`

The Zip folder will be used later in this demo.

## Linking the Application to Azure

Log in and Launch Azure Portal, and open the Cloud Shell.

Create a new resource group, choose a name. eg: appResourceGroup

`az group create --name appResourceGroup --location "West Europe"`

Create an appservice plan, this example will use the S1 pricing tier

`az appservice plan create --name nodeAppServicePlan --resource-group appResourceGroup --sku S1`

Create the web app in the appservice plan that was just created in the previous step. Note previous
names of Resource Group and AppServicePlan.

`az webapp create --resource-group appResourceGroup --plan nodeAppServicePlan --name demoNodeApp --runtime "NODE|6.9"`






