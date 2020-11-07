---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866091"
---
# <span data-ttu-id="60da8-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60da8-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="60da8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60da8-102">SYNOPSIS</span></span>
<span data-ttu-id="60da8-103">Ottiene un circuito di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="60da8-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60da8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60da8-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60da8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60da8-105">DESCRIPTION</span></span>
<span data-ttu-id="60da8-106">Il cmdlet **Get-AzureRmExpressRouteCircuit** viene usato per recuperare un oggetto Circuit ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="60da8-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="60da8-107">L'oggetto Circuit restituito può essere usato come input per altri cmdlet che operano su circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60da8-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="60da8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60da8-108">EXAMPLES</span></span>

### <span data-ttu-id="60da8-109">Esempio 1: ottenere il circuito ExpressRoute da eliminare</span><span class="sxs-lookup"><span data-stu-id="60da8-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="60da8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60da8-110">PARAMETERS</span></span>

### <span data-ttu-id="60da8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60da8-111">-DefaultProfile</span></span>
<span data-ttu-id="60da8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60da8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60da8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="60da8-113">-Name</span></span>
<span data-ttu-id="60da8-114">Il nome del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60da8-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60da8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60da8-115">-ResourceGroupName</span></span>
<span data-ttu-id="60da8-116">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60da8-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60da8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60da8-117">CommonParameters</span></span>
<span data-ttu-id="60da8-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60da8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60da8-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60da8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60da8-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60da8-120">INPUTS</span></span>

## <span data-ttu-id="60da8-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60da8-121">OUTPUTS</span></span>

### <span data-ttu-id="60da8-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60da8-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="60da8-123">Note</span><span class="sxs-lookup"><span data-stu-id="60da8-123">NOTES</span></span>

## <span data-ttu-id="60da8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60da8-124">RELATED LINKS</span></span>

[<span data-ttu-id="60da8-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60da8-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="60da8-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60da8-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="60da8-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60da8-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="60da8-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60da8-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
