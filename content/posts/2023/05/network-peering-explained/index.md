---
title: VNet Peerings - Traffic settings explained
date: 2023-04-04T12:00:00+02:00
description: An Azure CLI tool that let's you see the currently logged in user
draft: false
hiddenFromHomePage: false
tags:
    - Virtual Network
    - Subnets
    - Network Peering
    - User Defined Routes
categories:
    - Azure Networking
---

# Network Peering settings explained

## Our setup

We create a test environment with the following resources

- Virtual Network 1 (`vnet1`)
- Virtual Network 2 (`vnet2`)
- Network Peering between `vnet1` and `vnet2`
- Virtual Network Gateway in `vnet1`

## Example of vnet peering settings

Below Bicep code deploys a Virtual Network Peering.

```bicep
resource vnet1ToVnet2Peering 'Microsoft.Network/virtualNetworks/virtualNetworkPeerings@2021-03-01' = {
  name: 'vnet1ToVnet2'
  properties: {
    remoteVirtualNetwork: {
      id: vnet2.id
    }
    allowVirtualNetworkAccess: true
    allowForwardedTraffic: true
    allowGatewayTransit: false
    useRemoteGateways: false
  }
}
```

This Bicep template creates a peering between `vnet1` and `vnet2`. The `allowVirtualNetworkAccess` and `allowForwardedTraffic` properties are set to `true` to allow traffic to flow between the two virtual networks, and the `allowGatewayTransit` and `useRemoteGateways` properties are set to `false` to disable transit routing and to use the local gateways for each virtual network respectively.

### Traffic to remote virtual network

### Traffic forwarded from remote virtual network