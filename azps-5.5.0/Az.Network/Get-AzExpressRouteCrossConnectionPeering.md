---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187191"
---
# <span data-ttu-id="65931-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="65931-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="65931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65931-102">SYNOPSIS</span></span>
<span data-ttu-id="65931-103">Ottiene una configurazione di peering tra connessioni incrociate di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="65931-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="65931-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65931-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65931-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65931-105">DESCRIPTION</span></span>
<span data-ttu-id="65931-106">Il cmdlet **Get-AzExpressRouteCrossConnectionEndoing** recupera la configurazione di una relazione di peering per una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="65931-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="65931-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65931-107">EXAMPLES</span></span>

### <span data-ttu-id="65931-108">Esempio 1: Visualizzare la configurazione del peering per una connessione incrociata ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="65931-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="65931-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65931-109">PARAMETERS</span></span>

### <span data-ttu-id="65931-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65931-110">-DefaultProfile</span></span>
<span data-ttu-id="65931-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65931-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65931-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="65931-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="65931-113">Oggetto di connessione incrociata ExpressRoute contenente la configurazione di peering.</span><span class="sxs-lookup"><span data-stu-id="65931-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65931-114">-Name</span><span class="sxs-lookup"><span data-stu-id="65931-114">-Name</span></span>
<span data-ttu-id="65931-115">Nome della configurazione di peering da recuperare.</span><span class="sxs-lookup"><span data-stu-id="65931-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65931-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65931-116">CommonParameters</span></span>
<span data-ttu-id="65931-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65931-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65931-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65931-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65931-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="65931-119">INPUTS</span></span>

### <span data-ttu-id="65931-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="65931-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="65931-121">Il parametro 'ExpressRouteCrossConnection' accetta il valore di tipo 'PSExpressRouteCrossConnection' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="65931-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="65931-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65931-122">OUTPUTS</span></span>

### <span data-ttu-id="65931-123">Microsoft.Azure.Commands.Network.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="65931-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="65931-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="65931-124">NOTES</span></span>

## <span data-ttu-id="65931-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65931-125">RELATED LINKS</span></span>

[<span data-ttu-id="65931-126">Add-AzExpressRouteCrossConnectionEndoing</span><span class="sxs-lookup"><span data-stu-id="65931-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="65931-127">Remove-AzExpressRouteCrossConnectionEndoing</span><span class="sxs-lookup"><span data-stu-id="65931-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="65931-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="65931-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="65931-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="65931-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
