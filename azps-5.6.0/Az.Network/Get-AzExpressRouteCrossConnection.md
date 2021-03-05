---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967821"
---
# <span data-ttu-id="fba50-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fba50-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="fba50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba50-102">SYNOPSIS</span></span>
<span data-ttu-id="fba50-103">Ottiene una connessione incrociata di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="fba50-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="fba50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fba50-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba50-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fba50-105">DESCRIPTION</span></span>
<span data-ttu-id="fba50-106">Il cmdlet **Get-AzExpressRouteCrossConnection** viene usato per recuperare un oggetto di connessione incrociata ExpressRoute dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fba50-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="fba50-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fba50-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="fba50-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fba50-108">EXAMPLES</span></span>

### <span data-ttu-id="fba50-109">Esempio 1: Ottenere la connessione incrociata ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fba50-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="fba50-110">Esempio 2: Elencare le connessioni incrociate ExpressRoute usando un filtro</span><span class="sxs-lookup"><span data-stu-id="fba50-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="fba50-111">Questo cmdlet elenca tutte le connessioni incrociate ExpressRoute che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="fba50-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="fba50-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fba50-112">PARAMETERS</span></span>

### <span data-ttu-id="fba50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba50-113">-DefaultProfile</span></span>
<span data-ttu-id="fba50-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fba50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fba50-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fba50-115">-Name</span></span>
<span data-ttu-id="fba50-116">Nome della connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fba50-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="fba50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba50-117">-ResourceGroupName</span></span>
<span data-ttu-id="fba50-118">Nome del gruppo di risorse che contiene la connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fba50-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="fba50-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba50-119">CommonParameters</span></span>
<span data-ttu-id="fba50-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba50-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba50-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fba50-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba50-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="fba50-122">INPUTS</span></span>

### <span data-ttu-id="fba50-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fba50-123">None</span></span>
<span data-ttu-id="fba50-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fba50-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fba50-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fba50-125">OUTPUTS</span></span>

### <span data-ttu-id="fba50-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fba50-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="fba50-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="fba50-127">NOTES</span></span>

## <span data-ttu-id="fba50-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fba50-128">RELATED LINKS</span></span>

[<span data-ttu-id="fba50-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fba50-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)