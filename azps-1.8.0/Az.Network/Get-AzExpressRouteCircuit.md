---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: e37c8fdded8fa5e141138903e502e2e1b0f1a0f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678562"
---
# <span data-ttu-id="4ea79-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea79-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4ea79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ea79-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea79-103">Ottiene un circuito di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea79-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="4ea79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ea79-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea79-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ea79-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea79-106">Il cmdlet **Get-AzExpressRouteCircuit** viene usato per recuperare un oggetto Circuit ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ea79-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="4ea79-107">L'oggetto Circuit restituito può essere usato come input per altri cmdlet che operano su circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4ea79-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="4ea79-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ea79-108">EXAMPLES</span></span>

### <span data-ttu-id="4ea79-109">Esempio 1: ottenere il circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4ea79-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="4ea79-110">Ottenere un circuito ExpressRoute specifico con nome "testrg" e ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="4ea79-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="4ea79-111">Esempio 2: elencare i circuiti di ExpressRoute usando il filtro</span><span class="sxs-lookup"><span data-stu-id="4ea79-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="4ea79-112">Ottenere tutti i circuiti ExpressRoute il cui nome inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="4ea79-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="4ea79-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ea79-113">PARAMETERS</span></span>

### <span data-ttu-id="4ea79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea79-114">-DefaultProfile</span></span>
<span data-ttu-id="4ea79-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea79-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea79-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ea79-116">-Name</span></span>
<span data-ttu-id="4ea79-117">Il nome del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4ea79-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="4ea79-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea79-118">-ResourceGroupName</span></span>
<span data-ttu-id="4ea79-119">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4ea79-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="4ea79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea79-120">CommonParameters</span></span>
<span data-ttu-id="4ea79-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea79-122">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ea79-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea79-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ea79-123">INPUTS</span></span>

### <span data-ttu-id="4ea79-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea79-124">System.String</span></span>

## <span data-ttu-id="4ea79-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ea79-125">OUTPUTS</span></span>

### <span data-ttu-id="4ea79-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea79-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4ea79-127">Note</span><span class="sxs-lookup"><span data-stu-id="4ea79-127">NOTES</span></span>

## <span data-ttu-id="4ea79-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ea79-128">RELATED LINKS</span></span>

[<span data-ttu-id="4ea79-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea79-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4ea79-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea79-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="4ea79-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea79-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="4ea79-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea79-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)