---
title: Get started with Node.js
description: Get started building great apps in Microsoft Teams using Node.js
keywords: getting started node.js nodejs
---
# Get started on the Microsoft Teams platform with Node.js

[!include[Step 1 Intro](~/includes/get-started/step1-intro.md)]

This tutorial helps you get started with creating a Microsoft Teams app using Node.js. You can test the app by loading it into a 'Team' you have permissions for, or into a test tenant created using the Office Developer Program.

The steps to get started at a glance are as follows:

> [!div class="checklist"]
> * Prepare Microsoft Teams for development
> * Get prerequisites
> * Download the sample
> * Build and run the sample
> * Host the sample, either locally or on Azure (**plug the local app to ngrok or push to Azure**)
> * Deploy the sample app into Microsoft Teams platform (**by this time the manifest would be generated and they should be able to sideload the app**)
> * Configure the content visible in your app (**configure the content visible on the tab; TBD**)

Once you have your app running in the Teams platform, you can enhance it further by adding the following capabilities. Follow along this tutorial to learn how to add these capabilities to your app.

> [!div class="checklist"]
> * Add a bot to your application (**take the user through creation of a simple echo bot that echoes whatever you say**)
> * Add a connector to your application (**Not calling it Office 365 connector yet, but will guide the user to use it if they built an O365 connector before**)
> * Compose rich messages (**adding a simple compose extension**)

[!include[Get teams](~/includes/get-started/step1-prepare-for-dev.md)]

## Get prerequisites

To complete this tutorial, you need to get the following prerequisites:

* [Install Git](https://git-scm.com/downloads)
* [Install Node.js and NPM](https://nodejs.org/)

If you see options to add `git`, `node` and `npm` to the PATH during installation, choose to do so. It will be handy.

Verify your installation by running the following in a terminal window:

```bash
git --version
```

```bash
node -v
```

```bash
npm -v
```

## Download the sample

In a terminal window, run the following command to clone the sample repository to your local machine:

```bash
git clone https://github.com/OfficeDev/msteams-nodejs-hello-world
```

## Build and run the sample

Once the repo is cloned, change to the directory where you cloned the sample to:

```bash
cd msteams-nodejs-hello-world
```

You can use this terminal window to run the commands that follow in this tutorial.

In order to build the sample, you need to install all the dependencies first. Run the following command to get the dependencies installed:

```bash
npm install
```

You should see a bunch of dependencies getting installed. Once they are finished, you can run the following:

```bash
npm start
```

When the node app starts, it displays `App started listening on port 3333` on the terminal window.

> [!NOTE]
> If you see a different port number displayed in the message above, it is because you have a PORT environment variable set. You can continue to use that port or
> change your environment variable to 3333.

At this point, you can open a browser window and navigate to the following URLs to verify that all the app URLs are loading fine:

* [http://localhost:3333](http://localhost:3333)
* [http://localhost:3333/hello](http://localhost:3333/hello)
* [http://localhost:3333/first](http://localhost:3333/first)
* [http://localhost:3333/second](http://localhost:3333/second)

## Host the sample app

Remember apps in Microsoft Teams are web applications exposing one or more capabilities? For the Teams platform to load your app, your app must be reachable from the internet. To make your app reachable from the internet, you need to host your app. You can either host it in Microsoft Azure for free or create a tunnel to the local process run using ngrok.

### Hosting in Azure

Microsoft Azure lets you host your Node.js web application on a free tier using shared infrastructure. This will be sufficient to run our sample.

> [!TIP]
> If you have never used Azure before, you can get started by creating a new free account.
> Follow this guide to help you get started: [Azure developer guide](https://docs.microsoft.com/en-us/azure/guides/developer/azure-developer-guide?toc=/microsoftteams/platform/toc.json&bc=/microsoftteams/platform/breadcrumb/toc.json#understanding-accounts-subscriptions-and-billing).

To get your Node.js app hosted in Azure, you can follow the guide here: [Create a Node.js web app in Azure](/azure/app-service/app-service-web-get-started-nodejs?toc=/microsoftteams/platform/toc.json&bc=/microsoftteams/platform/breadcrumb/toc.json#launch-azure-cloud-shell).

> [!NOTE]
> You would skip the steps to clone the repo from the guide above, because we already are working with a Node.js sample app for Microsoft Teams.
> For your convenience, the link above takes you directly to the location where you should start from to host your app in Azure.

### Tunneling using ngrok

<!--
> [!div class="nextstepaction"]
> [Move to the next step](get-started-step2)
-->