# Delopying an App to Azure

Demo for deploying a test web app to Azure.

## Starting the application

To run locally use:

`npm start`

Currently the node application will run on https://localhost:1000

#### Zip the app with Bash
`zip -r myAppFiles.zip .`
#### Zip the app with PowerShell
`Compress-Archive -Path * -DestinationPath myAppFiles.zip`


## Linking the app with Azure

Log in and Launch Azure Portal, and open the Cloud Shell.

Create a new resource group, choose a name. eg appResourceGroup
`az group create --name appResourceGroup --location "West Europe"`








