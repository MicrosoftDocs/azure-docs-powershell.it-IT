---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475099"
---
# <span data-ttu-id="946a8-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="946a8-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="946a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="946a8-102">SYNOPSIS</span></span>
<span data-ttu-id="946a8-103">Ottiene un circuito di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="946a8-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="946a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="946a8-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="946a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="946a8-105">DESCRIPTION</span></span>
<span data-ttu-id="946a8-106">Il cmdlet **Get-AzExpressRouteCircuit** viene usato per recuperare un oggetto Circuit ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="946a8-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="946a8-107">L'oggetto Circuit restituito può essere usato come input per altri cmdlet che operano su circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="946a8-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="946a8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="946a8-108">EXAMPLES</span></span>

### <span data-ttu-id="946a8-109">Esempio 1: ottenere il circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="946a8-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="946a8-110">Ottenere un circuito ExpressRoute specifico con nome "testrg" e ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="946a8-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="946a8-111">Esempio 2: elencare i circuiti di ExpressRoute usando il filtro</span><span class="sxs-lookup"><span data-stu-id="946a8-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="946a8-112">Ottenere tutti i circuiti ExpressRoute il cui nome inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="946a8-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="946a8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="946a8-113">PARAMETERS</span></span>

### <span data-ttu-id="946a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946a8-114">-DefaultProfile</span></span>
<span data-ttu-id="946a8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="946a8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="946a8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="946a8-116">-Name</span></span>
<span data-ttu-id="946a8-117">Il nome del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="946a8-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="946a8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946a8-118">-ResourceGroupName</span></span>
<span data-ttu-id="946a8-119">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="946a8-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="946a8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946a8-120">CommonParameters</span></span>
<span data-ttu-id="946a8-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946a8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946a8-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="946a8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946a8-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="946a8-123">INPUTS</span></span>

### <span data-ttu-id="946a8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="946a8-124">System.String</span></span>

## <span data-ttu-id="946a8-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="946a8-125">OUTPUTS</span></span>

### <span data-ttu-id="946a8-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="946a8-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="946a8-127">Note</span><span class="sxs-lookup"><span data-stu-id="946a8-127">NOTES</span></span>

## <span data-ttu-id="946a8-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="946a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="946a8-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="946a8-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="946a8-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="946a8-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="946a8-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="946a8-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="946a8-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="946a8-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
