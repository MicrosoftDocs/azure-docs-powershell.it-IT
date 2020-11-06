---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513287"
---
# <span data-ttu-id="e152c-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e152c-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e152c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e152c-102">SYNOPSIS</span></span>
<span data-ttu-id="e152c-103">Ottiene un circuito di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="e152c-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e152c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e152c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e152c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e152c-105">DESCRIPTION</span></span>
<span data-ttu-id="e152c-106">Il cmdlet **Get-AzureRmExpressRouteCircuit** viene usato per recuperare un oggetto Circuit ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e152c-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="e152c-107">L'oggetto Circuit restituito può essere usato come input per altri cmdlet che operano su circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e152c-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="e152c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e152c-108">EXAMPLES</span></span>

### <span data-ttu-id="e152c-109">Esempio 1: ottenere il circuito ExpressRoute da eliminare</span><span class="sxs-lookup"><span data-stu-id="e152c-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="e152c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e152c-110">PARAMETERS</span></span>

### <span data-ttu-id="e152c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e152c-111">-Name</span></span>
<span data-ttu-id="e152c-112">Il nome del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e152c-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e152c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e152c-113">-ResourceGroupName</span></span>
<span data-ttu-id="e152c-114">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e152c-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e152c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e152c-115">-DefaultProfile</span></span>
<span data-ttu-id="e152c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e152c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e152c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e152c-117">CommonParameters</span></span>
<span data-ttu-id="e152c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e152c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e152c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e152c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e152c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e152c-120">INPUTS</span></span>

## <span data-ttu-id="e152c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e152c-121">OUTPUTS</span></span>

### <span data-ttu-id="e152c-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e152c-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e152c-123">Note</span><span class="sxs-lookup"><span data-stu-id="e152c-123">NOTES</span></span>

## <span data-ttu-id="e152c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e152c-124">RELATED LINKS</span></span>

[<span data-ttu-id="e152c-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e152c-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e152c-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e152c-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e152c-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e152c-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e152c-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e152c-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
