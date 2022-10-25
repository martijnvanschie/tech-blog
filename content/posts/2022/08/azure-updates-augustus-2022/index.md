---
title: Azure Updates - Augustus 2022
date: 2022-08-28T12:00:00+02:00
description: Welcome to the Azure Updates - August 2022 edition
draft: false
hiddenFromHomePage: false
tags:
    - Azure Functions
    - Network Security Groups
    - User-defined routes
    - Networking
    - Security
    - Private endpoints
    - Azure API Management
categories:
    - Azure Updates
---

Welcome to the Azure Updates - August 2022 edition.

Azure updates is a summary of the azure updates that I personally find the most interesting or are innovation i'm looking into for customers.

All topics are `General Availability` updates so can be used by everybody with an Azure subscription.

# The updates

## Control access to Azure Storage using "Resource instance rules"

A new layer of security has been added to Azure storage accounts that secure and control access to your account, **Resource instance rules**. With this new layer you can configure your storage account to only allow access from specific resource instances of a Azure services.

For example, you can specify access to your storage account from a Purview account.

This can be done on different levels

1. On a grouped scope (Tenant, Subscription or resource group)
2. On a specific instance by name

Below image shows this new setting in detail.

![alt text](202208-updates-resource-instance.png "Configure Resource instance access on Azure Storage")

### Resources

**Formal Azure Storage documentation**

[Grant access from Azure resource instances](https://docs.microsoft.com/en-us/azure/storage/common/storage-network-security?tabs=azure-portal#grant-access-from-azure-resource-instances)

## Private Endpoints now support User-defined routes and Network security groups

Prior to this update, when you configure a private endpoint for you Azure service in a subnet, it does not use the network policies like `Network Security Groups` and `User Defined Routes`. This updates changes that behavious by enabling these policies for private endpoints setting the `PrivateEndpointNetworkPolicies` property and enabling it on your subnet. 

### Resources

**Official announcement**

[General availability: Network security groups support for private endpoints](https://azure.microsoft.com/en-us/updates/general-availability-of-network-security-groups-support-for-private-endpoints/)

[General availability: User-defined routes support for private endpoints](https://azure.microsoft.com/en-us/updates/general-availability-of-user-defined-routes-support-for-private-endpoints/)

**Other resources**

[Manage network policies for private endpoints](https://docs.microsoft.com/en-us/azure/private-link/disable-private-endpoint-network-policy?tabs=network-policy-portal)

The following video shown the usage of this new feature and how Private Endpoints previously worked without this feature.

[Preview of Private Link NSG and UDR Support](https://www.youtube.com/watch?v=pZdlue6jwiI)

> So the demo does not go as smooth as it should but it does show the use case of the feature and what you can achieve with it.

## Azure API Management - expanded support for Azure Policy definitions

This small, but useful, update adds 11 built-in Azure Policy definitions for Azure API Management to the platform. As build-in policies are added to the platform the need to create, and maintain, custom policies is reduced.

### Resources

**Official announcement**

[Generally available: Azure API Management - expanded support for Azure Policy definitions](https://azure.microsoft.com/en-us/updates/generally-available-azure-api-management-expanded-support-for-azure-policy-definitions/)

**Other resources**

[Azure Policy built-in policy definitions for Azure API Management](https://learn.microsoft.com/en-us/azure/api-management/policy-reference)

**Note**: At the time of writing this article there where 11 policies defined on the page. This can differ when new policies have been added.

## Azure Function Blob Storage trigger is now event based

When using earlier versions of the `BlobTrigger()` for Azure Functions, the implementation was based on a pull model. This implies that the events being received where not always near realtime. The new version of `BlogTrigger()` is based on event grid and thus can be consumed near-realtime.

The make use of this new feature is pretty easy. You need to update the package `Microsoft.Azure.WebJobs.Extensions.Storage` to 5.x and then update the function to use events. This can be done using the tutorial as shared below.

### Resources

**Official announcement**

[Generally available: Azure Functions extension for Event Grid blob trigger](https://azure.microsoft.com/en-us/updates/generally-available-azure-functions-extension-for-event-grid-blob-trigger/)

**Other resources**

[Tutorial: Trigger Azure Functions on blob containers using an event subscription](https://learn.microsoft.com/en-us/azure/azure-functions/functions-event-grid-blob-trigger?tabs=csharp&pivots=programming-language-csharp)

