---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188505"
---
# <span data-ttu-id="49951-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="49951-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="49951-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49951-102">SYNOPSIS</span></span>
<span data-ttu-id="49951-103">Ottiene il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="49951-103">Gets private link service</span></span>

## <span data-ttu-id="49951-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49951-104">SYNTAX</span></span>

### <span data-ttu-id="49951-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49951-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49951-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="49951-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49951-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49951-107">DESCRIPTION</span></span>
<span data-ttu-id="49951-108">Il cmdlet **Get-AzPrivateLinkService** ottiene uno o più servizi di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="49951-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="49951-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49951-109">EXAMPLES</span></span>

### <span data-ttu-id="49951-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="49951-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="49951-111">Questo unifiedgroup ottiene un servizio di collegamento privato nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="49951-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="49951-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49951-112">PARAMETERS</span></span>

### <span data-ttu-id="49951-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49951-113">-DefaultProfile</span></span>
<span data-ttu-id="49951-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49951-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49951-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="49951-115">-ExpandResource</span></span>
<span data-ttu-id="49951-116">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="49951-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="49951-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="49951-117">-Name</span></span>
<span data-ttu-id="49951-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="49951-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49951-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49951-119">-ResourceGroupName</span></span>
<span data-ttu-id="49951-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49951-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="49951-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49951-121">CommonParameters</span></span>
<span data-ttu-id="49951-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49951-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49951-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49951-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49951-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49951-124">INPUTS</span></span>

### <span data-ttu-id="49951-125">System. String</span><span class="sxs-lookup"><span data-stu-id="49951-125">System.String</span></span>

## <span data-ttu-id="49951-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49951-126">OUTPUTS</span></span>

### <span data-ttu-id="49951-127">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="49951-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="49951-128">Note</span><span class="sxs-lookup"><span data-stu-id="49951-128">NOTES</span></span>

## <span data-ttu-id="49951-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49951-129">RELATED LINKS</span></span>
