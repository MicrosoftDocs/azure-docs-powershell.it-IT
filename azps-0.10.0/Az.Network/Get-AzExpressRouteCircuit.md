---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860830"
---
# <span data-ttu-id="a7e5d-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7e5d-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a7e5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e5d-103">Ottiene un circuito di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="a7e5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7e5d-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7e5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e5d-106">Il cmdlet **Get-AzExpressRouteCircuit** viene usato per recuperare un oggetto Circuit ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="a7e5d-107">L'oggetto Circuit restituito può essere usato come input per altri cmdlet che operano su circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="a7e5d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7e5d-108">EXAMPLES</span></span>

### <span data-ttu-id="a7e5d-109">Esempio 1: ottenere il circuito ExpressRoute da eliminare</span><span class="sxs-lookup"><span data-stu-id="a7e5d-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="a7e5d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7e5d-110">PARAMETERS</span></span>

### <span data-ttu-id="a7e5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e5d-111">-DefaultProfile</span></span>
<span data-ttu-id="a7e5d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e5d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7e5d-113">-Name</span></span>
<span data-ttu-id="a7e5d-114">Il nome del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a7e5d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e5d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7e5d-116">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a7e5d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e5d-117">CommonParameters</span></span>
<span data-ttu-id="a7e5d-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e5d-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e5d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e5d-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7e5d-120">INPUTS</span></span>

## <span data-ttu-id="a7e5d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7e5d-121">OUTPUTS</span></span>

### <span data-ttu-id="a7e5d-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7e5d-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a7e5d-123">Note</span><span class="sxs-lookup"><span data-stu-id="a7e5d-123">NOTES</span></span>

## <span data-ttu-id="a7e5d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7e5d-124">RELATED LINKS</span></span>

[<span data-ttu-id="a7e5d-125">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7e5d-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a7e5d-126">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7e5d-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a7e5d-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7e5d-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="a7e5d-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7e5d-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
