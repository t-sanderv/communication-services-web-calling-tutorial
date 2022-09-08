---
page_type: sample
languages:
- javascript
- nodejs
products:
- azure
- azure-communication-services
---

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ft-sanderv%2Fcommunication-services-web-calling-tutorial%2Fwithout-server-demo%2Fdeploy%2Fazuredeploy.json)
[![Deploy To Azure US Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.svg?sanitize=true)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ft-sanderv%2Fcommunication-services-web-calling-tutorial%2Fwithout-server-demo%2Fdeploy%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Ft-sanderv%2Fcommunication-services-web-calling-tutorial%2Fwithout-server-demo%2Fdeploy%2Fazuredeploy.json)


# ACS Calling Tutorial
This is a sample application to show how one can use the `azure@communication-calling` package to build a calling experience. The client-side application is a React based user interface.  

This is a sample application to show how one can use the `azure@communication-calling` package to build a calling experience.
The client-side application is a React based user interface. Alongside this front-end is a NodeJS web server application powered by ExpressJS that performs functionality like minting new user tokens for each Client participant. This separate server is necessary as you do not not want to make the **connection string** public, which gives everyone access to your Azure Communication Service resource.

## Prerequisites

1. [npm](https://www.npmjs.com/get-npm)
2. [Node.js (v14)](https://nodejs.org/en/download/)
3.  Create an Azure account with an active subscription. For details, see [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
4. Create an Azure Communication Services resource. For details, see [Create an Azure Communication Resource](https://docs.microsoft.com/azure/communication-services/quickstarts/create-communication-resource). You'll need to record your resource **connection string** for this quickstart.

## Code structure

* [`./Project/src`](./Project/src): Client side source code
* [`./Project/src/app/App.js`](./Project/src/app/App.js): Entry point into the client source code 
* [`./Project/webpack.config.js`](./Project/webpack.config.js): Project bundler. Has a simple local server for user token provisioning.
* [`./Project/config.json`](./Project/config.json): configuration file for specifying the connectiong string.

## Before running the sample for the first time
1. git clone https://github.com/Azure-Samples/communication-services-web-calling-tutorial
2. cd communication-services-web-calling-tutorial/Project
3. Get a connection string by provisioning an Azure Communication Services resource from the Azure portal. Use the connection string as value for key `connectionString` in config.json file.

## Local Run
1. Open a command prompt in the `Project` folder
2. `npm install`
3. `npm run start`
4. Open localhost:5000 in a browser. (Supported browsers are Chrome, Edge Chromium, and Safari)

## Deployment to Azure from VS Code
1. Open a command prompt in the `Project` folder
2. `npm install`
3. `npm run build`
4. Download the [Azure Plugin](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureresourcegroups) and the [Azure Static Web App Plugin](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurestaticwebapps) for VS Code.
5. In the Azure plugin pane, click `+`, and click `Create App Service Web App`.
6. Enter your subscription
7. Enter a unique app name
8. Select `Node 14` as the Runtime.

Your App Service should be configured

## Deployment to Azure

Use the blue buttons above.

## Resources

1. Documentation on how to use the ACS Calling SDK for Javascript can be found on https://docs.microsoft.com/en-gb/azure/communication-services/quickstarts/voice-video-calling/calling-client-samples?pivots=platform-web
2. ACS Calling SDK for Javascript API reference documentation can be found on https://docs.microsoft.com/en-us/javascript/api/azure-communication-services/@azure/communication-calling/?view=azure-communication-services-js
