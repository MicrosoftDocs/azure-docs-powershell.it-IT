---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186878"
---
# <span data-ttu-id="2cf61-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="2cf61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf61-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf61-103">Modifica un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2cf61-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2cf61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cf61-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf61-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2cf61-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf61-106">Il cmdlet **Set-AzExpressRouteCircuit** salva il circuito ExpressRoute modificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf61-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="2cf61-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cf61-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf61-108">Esempio 1: Modificare la chiave di servizio di un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2cf61-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="2cf61-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cf61-109">PARAMETERS</span></span>

### <span data-ttu-id="2cf61-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cf61-110">-AsJob</span></span>
<span data-ttu-id="2cf61-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2cf61-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf61-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf61-112">-DefaultProfile</span></span>
<span data-ttu-id="2cf61-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf61-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf61-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2cf61-115">Specifica **l'oggetto ExpressRouteCircuit** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf61-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf61-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf61-116">CommonParameters</span></span>
<span data-ttu-id="2cf61-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf61-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf61-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf61-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf61-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="2cf61-119">INPUTS</span></span>

### <span data-ttu-id="2cf61-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2cf61-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cf61-121">OUTPUTS</span></span>

### <span data-ttu-id="2cf61-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2cf61-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="2cf61-123">NOTES</span></span>

## <span data-ttu-id="2cf61-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cf61-124">RELATED LINKS</span></span>

[<span data-ttu-id="2cf61-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2cf61-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="2cf61-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="2cf61-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2cf61-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
