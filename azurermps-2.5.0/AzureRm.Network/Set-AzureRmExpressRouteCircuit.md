---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: a37502abcee157e9666a49ea5db5d2afe206aa8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866851"
---
# <span data-ttu-id="65882-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="65882-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65882-102">SYNOPSIS</span></span>
<span data-ttu-id="65882-103">Modifica un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="65882-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65882-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65882-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65882-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65882-105">DESCRIPTION</span></span>
<span data-ttu-id="65882-106">Il cmdlet **set-AzureRmExpressRouteCircuit** Salva il circuito ExpressRoute modificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="65882-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="65882-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65882-107">EXAMPLES</span></span>

### <span data-ttu-id="65882-108">Esempio 1: cambiare la ServiceKey di un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="65882-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="65882-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65882-109">PARAMETERS</span></span>

### <span data-ttu-id="65882-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65882-110">-AsJob</span></span>
<span data-ttu-id="65882-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="65882-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65882-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65882-112">-DefaultProfile</span></span>
<span data-ttu-id="65882-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65882-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65882-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="65882-115">Specifica l'oggetto **ExpressRouteCircuit** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="65882-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="65882-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65882-116">CommonParameters</span></span>
<span data-ttu-id="65882-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65882-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65882-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65882-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65882-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65882-119">INPUTS</span></span>

### <span data-ttu-id="65882-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="65882-121">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="65882-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="65882-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65882-122">OUTPUTS</span></span>

### <span data-ttu-id="65882-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="65882-124">Note</span><span class="sxs-lookup"><span data-stu-id="65882-124">NOTES</span></span>

## <span data-ttu-id="65882-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65882-125">RELATED LINKS</span></span>

[<span data-ttu-id="65882-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="65882-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="65882-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="65882-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="65882-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
