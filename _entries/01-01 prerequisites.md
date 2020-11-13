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

> Your username and password will be given by your proctor. Please use them to login to <https://portal.azure.com>.

### Azure Red Hat Openshift cluster

> You'll be provided with an existing Openshift cluster. Use your Azure credentials to login.
If you need to create your own cluster, its creation is described in the next chapter. The current version of Openshift expected for this lab is the version 4.3 (or superior).

### Tools

#### Azure Cloud Shell

> For this workshop we will use the Azure Cloud Shell accessible at <https://shell.azure.com> or by clicking on this icon in the top right of the Azure portal :
![Azure Cloud Shell](media/lab1/cloudshell_logo.png)

#### OpenShift CLI (oc)

> OpenShift CLI has been pre installed for this workshop

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