---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 415c084ebf6c1c83872a16d01ce4eb556f688103
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979614"
---
# <span data-ttu-id="7b144-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7b144-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="7b144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b144-102">SYNOPSIS</span></span>
<span data-ttu-id="7b144-103">Ottiene una configurazione peering tra connessioni ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b144-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="7b144-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b144-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b144-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b144-105">DESCRIPTION</span></span>
<span data-ttu-id="7b144-106">Il cmdlet **Get-AzExpressRouteCrossConnectionEndoing** recupera la configurazione di una relazione di peering per una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b144-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7b144-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b144-107">EXAMPLES</span></span>

### <span data-ttu-id="7b144-108">Esempio 1: Visualizzare la configurazione del peering per una connessione incrociata ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7b144-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="7b144-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b144-109">PARAMETERS</span></span>

### <span data-ttu-id="7b144-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b144-110">-DefaultProfile</span></span>
<span data-ttu-id="7b144-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b144-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b144-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b144-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7b144-113">Oggetto di connessione incrociata ExpressRoute contenente la configurazione di peering.</span><span class="sxs-lookup"><span data-stu-id="7b144-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="7b144-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7b144-114">-Name</span></span>
<span data-ttu-id="7b144-115">Nome della configurazione di peering da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7b144-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="7b144-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b144-116">CommonParameters</span></span>
<span data-ttu-id="7b144-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b144-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b144-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b144-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b144-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b144-119">INPUTS</span></span>

### <span data-ttu-id="7b144-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b144-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="7b144-121">Il parametro 'ExpressRouteCrossConnection' accetta il valore di tipo 'PSExpressRouteCrossConnection' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7b144-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="7b144-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b144-122">OUTPUTS</span></span>

### <span data-ttu-id="7b144-123">Microsoft.Azure.Commands.Network.Models.PS Pseudoing</span><span class="sxs-lookup"><span data-stu-id="7b144-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="7b144-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b144-124">NOTES</span></span>

## <span data-ttu-id="7b144-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b144-125">RELATED LINKS</span></span>

[<span data-ttu-id="7b144-126">Add-AzExpressRouteCrossConnectionEndoing</span><span class="sxs-lookup"><span data-stu-id="7b144-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7b144-127">Remove-AzExpressRouteCrossConnectionEndoing</span><span class="sxs-lookup"><span data-stu-id="7b144-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7b144-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b144-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="7b144-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b144-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
