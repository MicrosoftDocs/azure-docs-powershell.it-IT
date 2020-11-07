---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 9f40d9ce99db8640fcf98d48f8dc3920a8517b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853682"
---
# <span data-ttu-id="310fc-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="310fc-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="310fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="310fc-102">SYNOPSIS</span></span>
<span data-ttu-id="310fc-103">Ottiene il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="310fc-103">Gets private link service</span></span>

## <span data-ttu-id="310fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="310fc-104">SYNTAX</span></span>

### <span data-ttu-id="310fc-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="310fc-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="310fc-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="310fc-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="310fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="310fc-107">DESCRIPTION</span></span>
<span data-ttu-id="310fc-108">Il cmdlet **Get-AzPrivateLinkService** ottiene uno o più servizi di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="310fc-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="310fc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="310fc-109">EXAMPLES</span></span>

### <span data-ttu-id="310fc-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="310fc-110">Example</span></span>
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

<span data-ttu-id="310fc-111">Questo unifiedgroup ottiene un servizio di collegamento privato nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="310fc-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="310fc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="310fc-112">PARAMETERS</span></span>

### <span data-ttu-id="310fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310fc-113">-DefaultProfile</span></span>
<span data-ttu-id="310fc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="310fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="310fc-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="310fc-115">-ExpandResource</span></span>
<span data-ttu-id="310fc-116">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="310fc-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="310fc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="310fc-117">-Name</span></span>
<span data-ttu-id="310fc-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="310fc-118">The resource name.</span></span>

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

### <span data-ttu-id="310fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="310fc-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="310fc-120">The resource group name.</span></span>

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

### <span data-ttu-id="310fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310fc-121">CommonParameters</span></span>
<span data-ttu-id="310fc-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="310fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310fc-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="310fc-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310fc-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="310fc-124">INPUTS</span></span>

### <span data-ttu-id="310fc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="310fc-125">System.String</span></span>

## <span data-ttu-id="310fc-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="310fc-126">OUTPUTS</span></span>

### <span data-ttu-id="310fc-127">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="310fc-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="310fc-128">Note</span><span class="sxs-lookup"><span data-stu-id="310fc-128">NOTES</span></span>

## <span data-ttu-id="310fc-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="310fc-129">RELATED LINKS</span></span>
