---
sectionid: prereq
sectionclass: h2
title: Prerequisites
parent-id: intro
---


### Prerequisites

In order to realize the workshop, you will require several components. If you don't have them yet, you'll be guided to acquire them.

- an Azure subscription
- an Azure Red Had Openshift cluster
- an Azure DevOps organization

### Azure subscription

{% collapsible %}

Please use your username and password to login to <https://portal.azure.com>.

Also please authenticate your Azure CLI by running the command below on your machine and following the instructions.

```
az account show
az login
```

{% endcollapsible %}

### Azure Red Hat Openshift cluster

You'll need an Openshift Cluster. Either you'll be provided an existing one and credentials, or you have the possibility to create a new one on your own subscription. If you need to create your own cluster, its creation is described in the next chapter. The current version of Openshift expected for this lab is the version 4.3 (or superior).

### Tools

#### Azure Cloud Shell

You can either run command lines from your own computer (we recommend using bash) or you can use the Azure Cloud Shell accessible at <https://shell.azure.com> once you login with an Azure subscription.

{% collapsible %}

Head over to <https://shell.azure.com> and sign in with your Azure Subscription details.

{% endcollapsible %}

#### OpenShift CLI (oc)

> oc cli has been pre-installed on your Cloud Shell. Follow these steps only if you want to install oc cli on your own computer

You'll need to download the **latest OpenShift CLI (oc)** client tools for OpenShift 4.3. You can follow the steps below on the Azure Cloud Shell.

{% collapsible %}

```sh
cd ~

wget https://mirror.openshift.com/pub/openshift-v4/clients/ocp/latest/openshift-client-linux.tar.gz

mkdir openshift

tar -zxvf openshift-client-linux.tar.gz -C openshift

echo 'export PATH=$PATH:~/openshift' >> ~/.bashrc && source ~/.bashrc

```

The OpenShift CLI (oc) is now installed. You can use the **oc version** command to ensure the CLI is properly installed

```sh
oc version
```

{% endcollapsible %}

### Create an Azure DevOps account

You are going to use Azure DevOps for the software factory. You will create your own CI/CD pipelines.

{% collapsible %}

Go to <https://dev.azure.com> and sign-in with your Azure subscription credentials.

If this is your first time to provision an Azure DevOps account, you'll be taken through a quick wizard to create a new organization. Don't worry, it's free.

{% endcollapsible %}

### Install Openshift AzDo extension

In order to interact with the Openshift cluster you'll need the corresponding Azure DevOps extension.

{% collapsible %}

Head over to https://marketplace.visualstudio.com/items?itemName=redhat.openshift-vsts to install the extension on your organization

{% endcollapsible %}
