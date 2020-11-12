---
sectionid: createproject
sectionclass: h2
title: Create Project
parent-id: lab-todoapp
---

### Retrieve the login command and token

> You will be provided with a shared Openshift cluster. Use the URL and credentials your proctor provided you to connect to the Web console.

You are now connected to the OpenShift portal but we now need to find a way to be connected through the command line

{% collapsible %}

> **Note** Make sure you complete the [prerequisites](#prereq) to install the OpenShift CLI on the Azure Cloud Shell.

Once you're logged into the Web Console, click on the username on the top right, then click **Copy login command**.

![Copy login command](media/lab1/login-command.png)


Open the [Azure Cloud Shell](https://shell.azure.com) and paste the login command. You should be able to connect to the cluster.

![Login through the cloud shell](media/lab1/oc-login-cloudshell.png)

> the token you just used is a session token and is valid for 24 hours only. After that, you'll have to reconnect

{% endcollapsible %}

### Create a project

A project allows a community of users to organize and manage their content in isolation from other communities.

{% collapsible %}

It also automatically create a "namespace" and access rights around it. You can create a project with the Web portal or with the **oc new-project** command

```sh
oc new-project <PROJECT_NAME>
```

![Create new project](media/lab1/oc-newproject.png)

> You can also check in the OpenShift Web Portal that your newly created project is displayed.

{% endcollapsible %}

> **Resources**
> * [ARO Documentation - Access your services](https://docs.openshift.com/aro/getting_started/access_your_services.html)
> * [ARO Documentation - Getting started with the CLI](https://docs.openshift.com/aro/cli_reference/get_started_cli.html)
> * [ARO Documentation - Projects](https://docs.openshift.com/aro/dev_guide/projects.html)
