---
page_type: sample
languages:
- javascript
- nodejs
products:
- azure
- azure-communication-services
---

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2Fcommunication-services-web-calling-tutorial%2Fmain%2Fdeploy%2Fazuredeploy.json)
[![Deploy To Azure US Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.svg?sanitize=true)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2Fcommunication-services-web-calling-tutorial%2Fmain%2Fdeploy%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2Fcommunication-services-web-calling-tutorial%2Fmain%2Fdeploy%2Fazuredeploy.json)


# ACS Calling Tutorial

This is a sample application to show how one can use the `azure@communication-calling` package to build a calling experience.
The client-side application is a React based user interface. Alongside this front-end is a NodeJS web server application powered by ExpressJS that performs functionality like minting new user tokens for each Client participant. This separate server is necessary as you do not not want to make the **connection string** public, which gives everyone access to your Azure Communication Service resource.

## Prerequisites

1. [npm](https://www.npmjs.com/get-npm)
2. [Node.js (v14)](https://nodejs.org/en/download/)
3.  Create an Azure account with an active subscription. For details, see [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
4. Create an Azure Communication Services resource. For details, see [Create an Azure Communication Resource](https://docs.microsoft.com/azure/communication-services/quickstarts/create-communication-resource). You'll need to record your resource **connection string** for this quickstart.

## Code structure
- [`./Client/src`](./Client/src): Where the client code lives
- [`./Client/src/app/App.jsx`](./Client/src/app/App.jsx): Entry point into the Client sample 
- [`./Server/src/`](./Server/src/): Where the server code lives.
- [`./Server/src/app.ts`](./Server/src/app.ts): Entry point into the Server sample
- [`./Server/appsettings.json`](./Server/appsettings.json): Where to put your azure communication services connection string

## Before running the sample for the first time
1. Open an instance of PowerShell, Windows Terminal, Command Prompt or equivalent and navigate to the directory that you'd like to clone the sample to.
2. `git clone https://github.com/t-sanderv/communication-services-web-calling-tutorial`
3. `cd communication-services-web-calling-tutorial/Project`
4. Get a connection string by creating an Azure Communication Services resource from the Azure portal. Use the connection string as value for key `ResourceConnectionString` in `Server/appsettings.json` file.

## Local Run
1. Set your connection string in `Server/appsettings.json`
2. `npm run setup` from the root directory
3. `npm run start` from the root directory
4. Open `http://localhost:9000` in a browser. (Supported browsers are Chrome, Edge Chromium, and Safari)


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
