---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862805"
---
# <span data-ttu-id="8907a-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="8907a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8907a-102">SYNOPSIS</span></span>
<span data-ttu-id="8907a-103">Modifica un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8907a-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8907a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8907a-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8907a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8907a-105">DESCRIPTION</span></span>
<span data-ttu-id="8907a-106">Il cmdlet **set-AzExpressRouteCircuit** Salva il circuito ExpressRoute modificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="8907a-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="8907a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8907a-107">EXAMPLES</span></span>

### <span data-ttu-id="8907a-108">Esempio 1: cambiare la ServiceKey di un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8907a-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="8907a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8907a-109">PARAMETERS</span></span>

### <span data-ttu-id="8907a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8907a-110">-AsJob</span></span>
<span data-ttu-id="8907a-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8907a-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8907a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8907a-112">-DefaultProfile</span></span>
<span data-ttu-id="8907a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8907a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8907a-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8907a-115">Specifica l'oggetto **ExpressRouteCircuit** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8907a-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8907a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8907a-116">CommonParameters</span></span>
<span data-ttu-id="8907a-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8907a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8907a-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8907a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8907a-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8907a-119">INPUTS</span></span>

### <span data-ttu-id="8907a-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="8907a-121">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8907a-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="8907a-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8907a-122">OUTPUTS</span></span>

### <span data-ttu-id="8907a-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8907a-124">Note</span><span class="sxs-lookup"><span data-stu-id="8907a-124">NOTES</span></span>

## <span data-ttu-id="8907a-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8907a-125">RELATED LINKS</span></span>

[<span data-ttu-id="8907a-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8907a-127">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="8907a-128">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="8907a-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8907a-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
