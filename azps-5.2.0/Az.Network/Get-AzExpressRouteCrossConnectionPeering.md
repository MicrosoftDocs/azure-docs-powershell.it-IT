---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329752"
---
# <span data-ttu-id="0c3df-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0c3df-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="0c3df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c3df-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3df-103">Ottiene una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="0c3df-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="0c3df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c3df-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c3df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c3df-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3df-106">Il cmdlet **Get-AzExpressRouteCrossConnectionPeering** recupera la configurazione di una relazione di peering per una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0c3df-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="0c3df-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c3df-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3df-108">Esempio 1: visualizzare la configurazione peering per una connessione trasversale ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0c3df-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="0c3df-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c3df-109">PARAMETERS</span></span>

### <span data-ttu-id="0c3df-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3df-110">-DefaultProfile</span></span>
<span data-ttu-id="0c3df-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3df-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c3df-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c3df-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="0c3df-113">L'oggetto ExpressRoute Cross Connection che contiene la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="0c3df-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="0c3df-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c3df-114">-Name</span></span>
<span data-ttu-id="0c3df-115">Nome della configurazione peer da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0c3df-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="0c3df-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3df-116">CommonParameters</span></span>
<span data-ttu-id="0c3df-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3df-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3df-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c3df-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3df-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c3df-119">INPUTS</span></span>

### <span data-ttu-id="0c3df-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c3df-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="0c3df-121">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0c3df-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="0c3df-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c3df-122">OUTPUTS</span></span>

### <span data-ttu-id="0c3df-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="0c3df-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="0c3df-124">Note</span><span class="sxs-lookup"><span data-stu-id="0c3df-124">NOTES</span></span>

## <span data-ttu-id="0c3df-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c3df-125">RELATED LINKS</span></span>

[<span data-ttu-id="0c3df-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0c3df-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="0c3df-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0c3df-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="0c3df-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c3df-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="0c3df-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c3df-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
