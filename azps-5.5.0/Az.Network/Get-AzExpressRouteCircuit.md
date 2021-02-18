---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184751"
---
# <span data-ttu-id="744d3-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="744d3-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="744d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744d3-102">SYNOPSIS</span></span>
<span data-ttu-id="744d3-103">Ottiene un circuito Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="744d3-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="744d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="744d3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="744d3-105">DESCRIPTION</span></span>
<span data-ttu-id="744d3-106">Il cmdlet **Get-AzExpressRouteCircuit** viene usato per recuperare un oggetto circuito ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="744d3-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="744d3-107">L'oggetto circuito restituito può essere usato come input di altri cmdlet che operano sui circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="744d3-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="744d3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="744d3-108">EXAMPLES</span></span>

### <span data-ttu-id="744d3-109">Esempio 1: Ottenere il circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="744d3-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="744d3-110">Ottenere uno specifico circuito ExpressRoute con i nomi "testrg" e ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="744d3-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="744d3-111">Esempio 2: Elencare i circuiti ExpressRoute usando i filtri</span><span class="sxs-lookup"><span data-stu-id="744d3-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="744d3-112">Ottenere tutti i circuiti ExpressRoute il cui nome inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="744d3-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="744d3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="744d3-113">PARAMETERS</span></span>

### <span data-ttu-id="744d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744d3-114">-DefaultProfile</span></span>
<span data-ttu-id="744d3-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="744d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="744d3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="744d3-116">-Name</span></span>
<span data-ttu-id="744d3-117">Nome del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="744d3-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="744d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="744d3-119">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="744d3-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="744d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744d3-120">CommonParameters</span></span>
<span data-ttu-id="744d3-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744d3-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="744d3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744d3-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="744d3-123">INPUTS</span></span>

### <span data-ttu-id="744d3-124">System.String</span><span class="sxs-lookup"><span data-stu-id="744d3-124">System.String</span></span>

## <span data-ttu-id="744d3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="744d3-125">OUTPUTS</span></span>

### <span data-ttu-id="744d3-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="744d3-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="744d3-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="744d3-127">NOTES</span></span>

## <span data-ttu-id="744d3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="744d3-128">RELATED LINKS</span></span>

[<span data-ttu-id="744d3-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="744d3-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="744d3-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="744d3-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="744d3-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="744d3-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="744d3-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="744d3-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
