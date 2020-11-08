---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: ee140a968741269b8bebebeb7b179f8ad74e35c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203324"
---
# <span data-ttu-id="4d613-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d613-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="4d613-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d613-102">SYNOPSIS</span></span>
<span data-ttu-id="4d613-103">Ottiene un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4d613-103">Gets a network security group.</span></span>

## <span data-ttu-id="4d613-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d613-104">SYNTAX</span></span>

### <span data-ttu-id="4d613-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="4d613-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d613-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="4d613-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d613-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d613-107">DESCRIPTION</span></span>
<span data-ttu-id="4d613-108">Il cmdlet **Get-AzNetworkSecurityGroup** ottiene un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="4d613-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="4d613-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d613-109">EXAMPLES</span></span>

### <span data-ttu-id="4d613-110">Esempio 1: recuperare un gruppo di sicurezza di rete esistente</span><span class="sxs-lookup"><span data-stu-id="4d613-110">Example 1: Retrieve an existing network security group</span></span>
```powershell
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

<span data-ttu-id="4d613-111">Questo comando restituisce il contenuto del gruppo di sicurezza di rete Azure "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="4d613-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="4d613-112">Esempio 2: elencare i gruppi di sicurezza di rete esistenti tramite filtri</span><span class="sxs-lookup"><span data-stu-id="4d613-112">Example 2: List existing network security groups using filtering</span></span>
```powershell
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

<span data-ttu-id="4d613-113">Questo comando restituisce il contenuto dei gruppi di sicurezza di rete di Azure che iniziano con "NSG"</span><span class="sxs-lookup"><span data-stu-id="4d613-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="4d613-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d613-114">PARAMETERS</span></span>

### <span data-ttu-id="4d613-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d613-115">-DefaultProfile</span></span>
<span data-ttu-id="4d613-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d613-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d613-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4d613-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d613-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d613-118">-Name</span></span>
<span data-ttu-id="4d613-119">Specifica il nome del gruppo di sicurezza di rete ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d613-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4d613-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d613-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d613-121">Specifica il nome del gruppo di risorse a cui appartiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="4d613-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4d613-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d613-122">CommonParameters</span></span>
<span data-ttu-id="4d613-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d613-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d613-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d613-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d613-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d613-125">INPUTS</span></span>

### <span data-ttu-id="4d613-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4d613-126">System.String</span></span>

## <span data-ttu-id="4d613-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d613-127">OUTPUTS</span></span>

### <span data-ttu-id="4d613-128">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d613-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4d613-129">Note</span><span class="sxs-lookup"><span data-stu-id="4d613-129">NOTES</span></span>

## <span data-ttu-id="4d613-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d613-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d613-131">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d613-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="4d613-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d613-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="4d613-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d613-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


