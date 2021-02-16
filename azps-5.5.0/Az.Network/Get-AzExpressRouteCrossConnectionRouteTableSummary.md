---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187175"
---
# <span data-ttu-id="b76dc-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b76dc-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="b76dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b76dc-103">Ottiene un riepilogo della tabella di route di una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b76dc-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="b76dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b76dc-104">SYNTAX</span></span>

### <span data-ttu-id="b76dc-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="b76dc-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b76dc-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="b76dc-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b76dc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b76dc-107">DESCRIPTION</span></span>
<span data-ttu-id="b76dc-108">Il cmdlet **Get-AzExpressRouteCrossConnectionRouteTableSummary** recupera un riepilogo delle informazioni sui vicini BGP per un particolare contesto di routing.</span><span class="sxs-lookup"><span data-stu-id="b76dc-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="b76dc-109">Queste informazioni sono utili per determinare per quanto tempo è stato stabilito un contesto di routing e per il numero di prefissi di route annunciati dal router di peering.</span><span class="sxs-lookup"><span data-stu-id="b76dc-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="b76dc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b76dc-110">EXAMPLES</span></span>

### <span data-ttu-id="b76dc-111">Esempio 1: Visualizzare il riepilogo del percorso per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="b76dc-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="b76dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b76dc-112">PARAMETERS</span></span>

### <span data-ttu-id="b76dc-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="b76dc-113">-CrossConnectionName</span></span>
<span data-ttu-id="b76dc-114">Nome della connessione incrociata Express Route</span><span class="sxs-lookup"><span data-stu-id="b76dc-114">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76dc-115">-DefaultProfile</span></span>
<span data-ttu-id="b76dc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b76dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76dc-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b76dc-117">-DevicePath</span></span>
<span data-ttu-id="b76dc-118">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b76dc-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76dc-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b76dc-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b76dc-120">Express Route - Connessione incrociata</span><span class="sxs-lookup"><span data-stu-id="b76dc-120">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76dc-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b76dc-121">-PeeringType</span></span>
<span data-ttu-id="b76dc-122">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b76dc-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="b76dc-124">Nome del gruppo di risorse che contiene la connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b76dc-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76dc-125">CommonParameters</span></span>
<span data-ttu-id="b76dc-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76dc-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b76dc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76dc-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="b76dc-128">INPUTS</span></span>

### <span data-ttu-id="b76dc-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b76dc-129">None</span></span>
<span data-ttu-id="b76dc-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b76dc-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b76dc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b76dc-131">OUTPUTS</span></span>

### <span data-ttu-id="b76dc-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="b76dc-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="b76dc-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="b76dc-133">NOTES</span></span>

## <span data-ttu-id="b76dc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b76dc-134">RELATED LINKS</span></span>

[<span data-ttu-id="b76dc-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="b76dc-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="b76dc-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b76dc-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
